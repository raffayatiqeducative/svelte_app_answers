<script>
  export let name;

  import { Button } from 'flowbite-svelte';
  import { Spinner } from 'flowbite-svelte';

</script>

<main>
  <h1>Login</h1>

  <div class="login-inputs">
    <label for="email">Email</label>
    <input type="email" name="email" use:validators={[required, email]} />
    <label for="password">Password</label>
    <input type="password" name="password" use:validators={[required]} />
  </div>
  
  <Button>Login</Button>

  <!-- <Spinner /> -->
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

</style>