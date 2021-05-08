<template>
    <div
        class="w-60 mx-auto flex flex-wrap 
        gap-8 border-solid border-2 border-black mt-10 p-4 items-center justify-items-center
        select-none
        "
    >
        
        <div class="flex flex-wrap gap-6 justify-center">
          <input
            class="border-solid border border-gray-500 px-2"
            type="text"
            v-model="inputValue"
        />
            <phone-button
                v-for="(button, index) in buttons"
                :button="button"
                :key="index"
                @click="clickHandler(button)"
            >
            </phone-button>
        </div>
    </div>
</template>

<script>
import PhoneButton from "./PhoneButton.vue";
export default {
    components: { PhoneButton },
    data() {
        return {
            inputValue: "",
            buttons: [
                {
                    mainButton: "1",
                    subButton: "",
                },
                {
                    mainButton: "2",
                    subButton: "ABC",
                },
                {
                    mainButton: "3",
                    subButton: "DEF",
                },
                {
                    mainButton: "4",
                    subButton: "GHI",
                },
                {
                    mainButton: "5",
                    subButton: "JKL",
                },
                {
                    mainButton: "6",
                    subButton: "MNO",
                },

                {
                    mainButton: "7",
                    subButton: "PQRS",
                },

                {
                    mainButton: "8",
                    subButton: "TUV",
                },
                {
                    mainButton: "9",
                    subButton: "WXYZ",
                },

                {
                    mainButton: "*",
                    subButton: "",
                },

                {
                    mainButton: "0",
                    subButton: "",
                },

                {
                    mainButton: "#",
                    subButton: "",
                },
                {
                    mainButton: "⌫",
                    subButton: "",
                },
                {
                    mainButton: "C",
                    subButton: "",
                },
            ],
        };
    },
    methods: {
        clickHandler(button) {
          if(button.mainButton == 'C') {
            this.inputValue = this.inputValue.substring(0, this.inputValue.length - 1);
            return;
          }
          if (button.mainButton == '⌫') {
            this.inputValue = '';
            return;
          }
          this.inputValue += button.mainButton;
        }
    }
};
</script>

<style></style>
