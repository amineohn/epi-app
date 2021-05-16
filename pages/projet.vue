<template>
  <fragment>
    <Navigation />
    <div class="fade-in">
      <div class="columns is-desktop">
        <div class="column is-four-fifths">
          <section class="section">
            <div class="container">
              <div class="columns">
                <div class="column">
                  <h1 class="title"><code>EPI HELP&CIE</code></h1>
                  <h2 class="subtitle" style="font-size: 17px;padding-top: 2%;text-align: justify;">
                   sera une véritable révolution pour les personnes atteintes d'épilepsie. C'est un bracelet possédant de nombreuses fonctionnalités. Il consiste à réduire les risques encourus par les malades lors d'une crise d'épilepsie. Le bijou doit être esthétique, raffiné et unisexe afin de plaire au genre masculin et féminin. Puisqu'une crise d'épilepsie peut avoir lieu à tout moment et en tout lieu, le malade devra porter le bracelet 24h/24h. Pour cela, le bracelet sera waterproof. Il existe 2 systèmes d'activation : le bracelet pourra détecter la chute ou les tremblements grâce à des capteurs, ou bien le malade pourra activer lui-même le processus de secours en appuyant sur un bouton lorsqu'il sentira la crise arriver, c'est ce qu'on appelle l'aura. Une vibration ainsi qu'un son seront produits par le bijou afin d'en informer la personne. En cas d'erreur, un système d'annulation est proposé. Suite à l'activation, le bracelet contacte les secours et partage la géolocalisation. De plus, un message audio d'alerte est diffusé par le bracelet. Ce message informe l'entourage de la situation et indique les consignes de sécurité à appliquer.
                  </h2>
                </div>

              </div>
            </div>
          </section>
        </div>
      </div>
    </div>
    <Footer />
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