<template>
<div>
  <div class="container">
      <ul class="nav nav-pills nav-justified mb-3" id="ex1" role="tablist">
  <li class="nav-item" role="presentation">
    <a class="nav-link " id="tab-login" data-mdb-toggle="pill" href="/" role="tab"
      aria-controls="pills-login" aria-selected="true">Login</a>
  </li>
  <li class="nav-item" role="presentation">
    <nuxt-link class="nav-link active" id="tab-register" data-mdb-toggle="pill" to="/register" role="tab"
      aria-controls="register" aria-selected="false">Sign up</nuxt-link>
  </li>
</ul>
      <form>
      <!-- Name input -->
       <div class="form-outline mb-4 ">
             <input type="text" id="registerName" class="form-control " placeholder="Name" />
             <label class="form-label" for="registerName"></label>
        </div>
   
      <!-- Username input -->
      <div class="form-outline mb-4">
        <input type="text" id="registerUsername" class="form-control" placeholder="Username" />
        <label class="form-label" for="registerUsername"></label>
      </div>

      <!-- Email input -->
      <div class="form-outline mb-4">
        <input type="email" id="registerEmail" class="form-control" placeholder="Email" />
        <label class="form-label" for="registerEmail"></label>
      </div>

      <!-- Password input -->
      <div class="form-outline mb-4">
        <input type="password" id="registerPassword" class="form-control" placeholder="Password" />
        <label class="form-label" for="registerPassword"></label>
      </div>

      <!-- Repeat Password input -->
      <div class="form-outline mb-4">
        <input type="password" id="registerRepeatPassword" class="form-control" placeholder="Repeat password" />
        <label class="form-label" for="registerRepeatPassword"></label>
      </div>

      <!-- Checkbox -->
      <div class="form-check d-flex justify-content-center mb-4">
        <input class="form-check-input me-2" type="checkbox" value="" id="registerCheck" checked
          aria-describedby="registerCheckHelpText" />
        <label class="form-check-label" for="registerCheck">
          I have read and agree to the terms
        </label>
      </div>

      <!-- Submit button -->
      <button type="submit" class="btn btn-primary btn-block mb-3">Sign up</button>
    </form>

</div>
<!-- Pills content -->
</div>
</template>

<script>
export default {

}
</script>

<style>

</style>