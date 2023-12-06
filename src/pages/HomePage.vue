<template>
  <section class="container-fluid background-image" style="height: 100vh;">
    <div class="row">
      <div class="col-12 text-center">Hello</div>
      <!-- Text Area -->
      <div class="col-6">List
        <div class="col-12"><textarea name="" id="" cols="30" rows="10"></textarea></div>
      </div>
      <!-- List -->
      <div class="col-6">
        <div class="col-12">
          <form action="" @submit.prevent="createToDo()">
                <div>
                  <label for="ToDo">Todo</label>
                  <input type="text" id="description" minlength="3" maxlength="30" required name="description">
                  <button type="submit">Submit</button>
                </div>
              </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { logger } from "../utils/Logger";

export default {
  setup() {
    return {
       createToDo() {
        
        logger.log('button pressed')
        
      },
    }
  }
}
</script>

<style scoped lang="scss">
.home {
  display: grid;
  height: 80vh;
  place-content: center;
  text-align: center;
  user-select: none;

  .home-card {
    width: clamp(500px, 50vw, 100%);

    >img {
      height: 200px;
      max-width: 200px;
      width: 100%;
      object-fit: contain;
      object-position: center;
    }
  }
}
.background-image{
  background-image: url(https://images.unsplash.com/photo-1682687982204-f1a77dcc3067?q=80&w=3387&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D) ;
  object-fit: cover;
  object-position: center;

}
</style>
