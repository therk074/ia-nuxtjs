<template>
  <div>
    <h1>My Heroes</h1>
    <ul v-for="(hero, index) in heroes" :key="index">
      <li @click="selectHero(hero.name)">{{ hero.number }} {{ hero.name }}</li>
    </ul>

    My hero is <u>{{ hero }}</u>
  </div>
</template>

<script>
export default {
  data() {
    return {
      heroes: [
        { number: "11", name: "Dr Nice" },
        { number: "12", name: "necromancer" },
        { number: "13", name: "Bombbasto" },
        { number: "14", name: "Celeritas" },
        { number: "15", name: "Magneta" },
        { number: "16", name: "RubberMan" },
        { number: "17", name: "Dynama" },
        { number: "18", name: "Dr IQ" },
        { number: "19", name: "Magma" },
        { number: "20", name: "Tornado" },
      ],
      hero: null,
    };
  },
  methods: {
    selectHero(heroName) {
      this.hero = heroName;
    },
  },
};
</script>