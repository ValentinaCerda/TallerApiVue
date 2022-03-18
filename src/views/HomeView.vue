<template>
  <h1 class="mt-5">Letra de Canciones</h1>

  <div class="container">
    <div class="row">
      <div class="col-6">
        <form>
          <div class="mb-3">
            <label for="artista" class="form-label">Artista</label>
            <input type="text" class="form-control" required>
          </div>
          <div class="mb-3">
            <label for="cancion" class="form-label">Canción</label>
            <input type="text" class="form-control" required>
          </div>
          <div class="d-grip gap-2">
            <router-link :to="`/LyricsView/${lyrics}`"  class="btn btn-success">Buscar</router-link>
          </div>
        </form>
      </div>
      
    </div>
  </div>
</template>

<script>

</script>
