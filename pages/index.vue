<template>
  <div>
    <Navbar />
    <Header />
    <main>
      <AboutMe />
    </main>
  </div>
</template>

<script>
import AboutMe from '@/components/AboutMe'
import Header from '@/components/Header'
import Navbar from '@/components/Navbar'

export default {
  components: {
    Navbar,
    Header,
    AboutMe,
  },
}
</script>
