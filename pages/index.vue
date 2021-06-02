<template>
  <fragment>
    <Navigation />
    <section class="section">
      <div class="container">
        <div class="fade-in">
          <div style="margin-top: 15px" class="columns is-desktop">
            <div class="column is-four-fifths">
              <section class="section">
                <div class="container">
                  <div style="align-items: center" class="columns">
                    <div class="column">
                      <h1 class="title">Qui sommes nous?</h1>
                      <h2 class="subtitle" style="text-align: justify">
                        Nous sommes Anaëlle et Romane, deux lycéennes pleines
                        d’ambition et de motivation. Nous sommes lauréates du
                        concours
                        <span class="big-text">&nbsp;Science Factor&nbsp;</span>, un concours visant à faire
                        émerger des idées et des projets d’innovation citoyens
                        chez les étudiants de la sixième à la terminale. Nous
                        nous sommes lancés dans la réalisation de notre projet
                        grâce à l’accompagnement offert par les partenaires de
                        Science Factor, dont Orange. Notre objectif est de
                        pouvoir venir en aide aux personnes atteintes
                        d’épilepsie, en leur proposant notre projet.
                      </h2>
                    </div>
                    <div class="column">
                      <img
                        style="border-radius: 1em"
                        src="@/assets/img/science.png"
                      />
                    </div>
                  </div>
                </div>
              </section>
            </div>
          </div>
          <Footer />
        </div>
      </div>
    </section>
  </fragment>
</template>

<script>
export default {
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();
      setTimeout(() => this.$nuxt.$loading.finish(), 2000);
    });
  },
};
</script>

<style>
</style>
