<script lang="ts">
  import FileInput from "$lib/components/form-components/FileInput.svelte";
</script>

<div class="center">
  <div class="card">
    <h2 class="center-text">Admin Stuff</h2>
    <div class="card" style="width: fit-content">
      <form class="stack" action="POST">
        <FileInput name="scryfall-data" label="Upload Scryfall data" accept=".json" required />
        <button type="submit" style="width: 100%">Upload</button>
      </form>
    </div>
  </div>
</div>
