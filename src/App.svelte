<script>
  export let name;

  import { Button } from 'flowbite-svelte';
</script>

<main>
  <h1>Login</h1>
  <br>

  <label for="email">Email</label>
  <br>
  <input type="email" name="email" use:validators={[required, email]} />
  <br>
  <label for="password">Password</label>
  <br>
  <input type="password" name="password" use:validators={[required]} />
  <br><br>
  <div>
    <Button>Login</Button>
  </div>

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