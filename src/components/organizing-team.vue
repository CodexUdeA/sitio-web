<template>
  <section id="team" class="organizing-team">
    <div class="title">
      <h1 class="organizing-team__title">Equipo organizador</h1>
    </div>
    <div class="container">
      <div class="row center-xs">
        <div
          v-for="member in team"
          :key="member.name"
          class="organizing-team__item col-xs-12 col-sm-6 col-md-4 col-lg-3">
          <team-card :team-member="member"/>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import team from '../assets/data/team'
import TeamCard from '../components/team-card'

export default {
  name: 'organizing-team',
  components: {
    TeamCard
  },
  data () {
    return {
      team
    }
  }
}
</script>

<style lang="scss">
@import '../styles/vars';
@import '../styles/functions';

.organizing-team {
  background-color: color(white);
  padding: 88px 0;

  &__title {
    color: color(astronaut);
  }

  &__item {
    padding-bottom: 1rem;
  }
}
</style>
