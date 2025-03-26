<template>
  <div
    class="bg-gradient-to-b from-pink-100 to-blue-100 min-h-screen flex flex-col items-center p-6"
  >
    <h1 class="text-3xl font-extrabold text-pink-600 mb-6 drop-shadow-lg">
      Promoções do Bryan Bet
    </h1>
    <div class="flex flex-direction-row justify-center gap-10">
      <div class="flex justify-center align-center">
        <img src="@/assets/bryanbet.jpg" alt="" />
      </div>
      <div class="w-full max-w-md">
        <Accordion
          v-for="(promo, index) in promos"
          :key="index"
          :title="promo.title"
        >
          <p class="text-gray-700 text-lg leading-relaxed">
            {{ promo.description }}
          </p>
        </Accordion>
      </div>
      <div class="flex justify-center align-center">
        <img src="@/assets/bryanbet.jpg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
import Accordion from '@/components/AccordionItem.vue';

export default {
  components: { Accordion },
  data() {
    return {
      promos: [
        {
          title: 'Ganhe o Triplo com o Dobro',
          description:
            'Deposite o dobro e receba o triplo de saldo para apostar!',
        },
        {
          title: 'Indique e Ganhe Chances em Dobro',
          description: 'Cada indicação dobra suas chances de ganhar!',
        },
        {
          title: 'Seja Indicado e Ganhe o Triplo de Chances',
          description: 'Se alguém te indicar, suas chances triplicam!',
        },
        {
          title: 'Tudo ou Nada',
          description:
            'Aposte tudo e tenha a chance de ganhar tudo ou perder tudo!',
        },
        {
          title: 'Promoção do Aniversário Atrasado',
          description:
            'Se notificarmos seu aniversário atrasado, seu valor triplica!',
        },
        {
          title: 'Horas Bugadas',
          description:
            'Assinando o VIP, todo dia você recebe uma notificação da hora bugada!',
        },
      ],
    };
  },
};
</script>

<style>
body {
  background-color: #fce4ec;
  font-family: 'Arial', sans-serif;
}
</style>
