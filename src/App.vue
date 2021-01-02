<template>

    <Header />
    <Main />
    <Footer />
    <Aside />

</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import Aside from './components/Aside.vue';





export default {
  name: 'App',
  components: {
    HelloWorld,
    Header,
    Main,
    Footer,
    Aside,
  }
}
</script>
