<template>
  <div class="flex flex-col h-screen shadow-2xl overflow-hidden">
    <Header class="w-full" />
    <main class="flex-1 overflow-y-scroll">
      <Home/>
      <Tabs/>
    </main>
    <Footer class="w-full shadow-2xl h-16" />
</div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
