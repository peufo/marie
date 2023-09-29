<script lang="ts">
  import JSConfetti from 'js-confetti'
  import { onMount } from 'svelte'

  onMount(() => {
    const jsConfetti = new JSConfetti()
    let count = 3

    const confetti = () => {
      count--
      jsConfetti.addConfetti({})
      if (count > 0) {
        setTimeout(confetti, 400)
      }
    }
    confetti()
  })
</script>

<div class="p-4">
  <h1 class="text-center text-3xl">Génial, vous êtes invité !</h1>

  <div class="rounded-xl border shadow-2xl mt-8 p-4 flex flex-col gap-4">
    <h2 class="text-center text-3xl">Menu</h2>
    <hr />

    <p>Le plat sera composé de :</p>
    <ul class="list-disc pl-6">
      <li>Harmonie de pommes de terre rissolées</li>
      <li>Légumes verts croquants</li>
      <li>Pépites de volaille dorées</li>
    </ul>

    <p>Le tout accompagné d'une salade fraîche et délicate</p>

    <img src="/patates.jpg" alt="patates" class="rounded" />
  </div>
</div>
