<template>
  <main class="flex justify-center items-center h-screen bg-gray-100">
    <!-- Quiz container -->
    `
    <div
      class="bg-white container flex-none relative shadow-lg rounded-lg px-12 py-6 overflow-hidden"
    >
      <!--Decoration-->
      <div>
        <div
          class="triangle2 absolute transform -rotate-3 -right-3 -top-3 object-none"
        ></div>
        <div
          class="triangle absolute transform rotate-6 -left-3 -top-3 object-none"
        ></div>
      </div>

      <!-- Content -->
      <div class="relative">
        <!--- Score container ---->
        <div class="text-right text-gray-800">
          <p class="text-sm leading-3">Score</p>
          <p class="font-bold">score</p>
        </div>

        <!-- display the current Question-->
        <div
          class="rounded-lg p-2 bg-gray-100 newmorph-1 text-center text-gray-800 font-bold"
        >
          <div class="bg-white p-5">currentQuestion.question</div>
        </div>

        <!-- Container of all the Options -->
        <div class="mt-8">
          <!-- Container of one Option -->
          <div v-for="(a, key) in questions[0].options" :key="key">
            <!-- Reward +10 -->
            <div
              class="bg-blue-600 p-1 transform rotate-45 rounded-lg h-10 w-10 text-white font-bold absolute right-0 -top-0 shadow-md"
            >
              <p class="transform -rotate-45">+10</p>
            </div>
            <!-- End of Reward-->

            <div class="rounded-lg font-bold flex p-2">
              <!-- Option -->
              <label for="" class="flex items-center pl-6">
                <input type="radio" name="" id="" class="hidden" />
                choice {{ a.key }}
              </label>
            </div>
          </div>
          <!---end of option-->
        </div>
        <!--end of Options container-->

        <!-- Progress Indicator Container -->
        <div class="mt-8 text-center">
          <div class="h-1 w-12 bg-gray-800 rounded-full mx-auto"></div>
          <p class="font-bold text-gray-800">
            questionCounter / questions.length
          </p>
        </div>
        <!-- End of Progress Bar-->
      </div>
      <!-- End of Content-->
    </div>
    <!--end of Quiz Container-->
  </main>
</template>
<!--- Local CSS  style-->

<style scoped>
.newmorph-1 {
  box-shadow: 6px 6px 18px rgba(0, 0, 0, 0.09), -6px -6px 18px #ffff;
}
.container {
  max-width: 400px;
  border-radius: 25px;
}
.triangle {
  border: 5rem solid rgb(85, 149, 201);
  border-left-width: 7rem;
  border-right-width: 9rem;
  border-right-color: rgba(255, 255, 255, 0);
  border-bottom-color: rgba(255, 255, 255, 0);
}
.triangle2 {
  border: 5rem solid rgb(221, 240, 94);
  border-right-width: 7rem;
  border-left-width: 9rem;
  border-left-color: rgba(255, 255, 255, 0);
  border-bottom-color: rgba(255, 255, 255, 0);
}
</style>
<script>
export default {
  name: "HelloWorld",
  props: {},
  data() {
    return {
      questions: [
        {
          question: "Qa",
          answer: "Aa",
          options: ["a", "b", "c", "d"],
        },
        {
          question: "Q b",
          answer: "Ab",
          options: ["a", "b", "c", "d"],
        },
        {
          question: "Q c",
          answer: "ac",
          options: ["a", "b", "c", "d"],
        },
        {
          question: "Q d",
          answer: "A d",
          options: ["a", "b", "c", "d"],
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
