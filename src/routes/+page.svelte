<script lang="ts">
  import { onMount } from 'svelte'

  let width = 0
  onMount(() => {
    const interval = setInterval(() => {
      width = width ? 0 : 100
    }, 1500)
    return () => {
      clearInterval(interval)
    }
  })
</script>

<h1 class="text-6xl text-center p-4">La cuisine est terminé</h1>
<h2 class="text-xl text-center">( presque )</h2>

<section class="my-8 relative">
  <img src="/cuisine_photo.jpg" alt="cuisine" />

  <div
    class="absolute top-0 h-full w-full bg-cover transition-all duration-700"
    style:width="{width}%"
    style:background-image="url(/cuisine_blender.png)"
  />
</section>

<section class="p-4">
  <p class="mb-2">
    Pour l'occasion, vous aurrez peut-être la chance d'être invité à la grande
    cérémonie d'inauguration qui aurra lieu pas plus tard que ce soir. 🥳🥳🥳
  </p>

  <p>
    Mais comment savoir si je suis invité me direz-vous. C'est très simple, il
    vous suffit de répondre correctement à la question suivante :
  </p>

  <div class="flex justify-center">
    <img src="/arrow.png" alt="arrow" class="h-20" />
  </div>
</section>

<section class="p-4 pb-36 flex flex-col gap-4">
  <h3 class="text-2xl text-center">Êtes-vous amoureuse de Jonas ?</h3>

  <div class="flex justify-evenly">
    <a
      href="/bad"
      class="rounded-lg shadow-lg px-4 py-2 border border-red-800 bg-red-400 uppercase"
    >
      C'est mort
    </a>
    <a
      href="/menu"
      class="rounded-lg shadow-lg px-4 py-2 border border-green-800 bg-green-400 uppercase"
    >
      C'est clair
    </a>
  </div>
</section>
