<template>
  <div id="app" class="py-5 has-background-black">
    <div class="container">
      <section>
        <h1 class="title is-1 has-text-white">
          Bem-vindo(a) ao mapa de front-end
        </h1>

        <p class="has-text-white">
          Esse é um site feito para que você possa controlar o seus estudos de
          front-end 😉
        </p>
      </section>

      <section class="mt-5">
        <b-steps
          :position="position"
          :label-position="labelPosition"
          mobile-mode="compact"
          :size="size"
          :has-navigation="false"
          v-model="step"
          vertical
        >
          <b-step-item
            v-for="(skill, index) in skills"
            :key="index"
            :label="skill.skill"
            :step="index"
            clickable="true"
          >
            <b-checkbox v-model="checkboxGroup" native-value="Silver">
              DNS
            </b-checkbox>

            <b-checkbox value="2" v-model="checkboxGroup" native-value="Flint">
              Hospedagem
            </b-checkbox>

            <b-checkbox v-model="checkboxGroup" native-value="Vane">
              HTTP
            </b-checkbox>

            <b-checkbox v-model="checkboxGroup" native-value="Billy">
              Como a internet funciona
            </b-checkbox>
          </b-step-item>
        </b-steps>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      skills: [
        {
          skill: 'internet',
          isComplete: false,
        },
        {
          skill: 'html',
          isComplete: false,
        },
        {
          skill: 'css',
          isComplete: false,
        },
        {
          skill: 'javascript',
          isComplete: false,
        },
        {
          skill: 'git',
          isComplete: false,
        },
        {
          skill: 'github',
          isComplete: false,
        },
        {
          skill: 'gerenciamento de pacotes',
          isComplete: false,
        },
        {
          skill: 'pre processadores css',
          isComplete: false,
        },
        {
          skill: 'arquitetura',
          isComplete: false,
        },
        {
          skill: 'frameworks',
          isComplete: false,
        },
        {
          skill: 'css moderno',
          isComplete: false,
        },
      ],
      labelPosition: 'bottom',
      position: null,
      size: 'is-medium',
      step: 0,
    };
  },
};
</script>

<style scoped></style>
