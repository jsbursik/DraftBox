<script lang="ts">
  let { label, name, required = false, accept = undefined } = $props();
</script>

<div class="file-input-wrapper">
  <label class="file-input" for={name}>{label}</label>
  <input type="file" {name} id={name} {accept} {required} />
</div>

<style>
  .file-input-wrapper {
    position: relative;
    width: 16rem;
  }

  .file-input-wrapper > input[type="file"] {
    position: absolute;
    inset: 0;
    opacity: 0;
    cursor: pointer;
    z-index: 1;
  }

  .file-input {
    display: grid;
    place-items: center;
    padding: 2rem;
    margin: 0;
    width: 100%;
    background: var(--color-bg);
    border: 2px solid var(--color-border);
    border-radius: var(--radius-lg);
    pointer-events: none; /* Let clicks pass through to the input */
  }
</style>
