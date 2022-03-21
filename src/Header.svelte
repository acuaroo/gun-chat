<script>
  import { username, user } from './user';

  function signout() {
    user.leave();
    username.set('');
  }
</script>

<header>
<h1>harmony</h1>
  {#if $username}
    <div class="user-bio">
      
      <span>hey <strong>{$username}</strong></span>
      <img src={`https://avatars.dicebear.com/api/bottts/${$username}.svg`} alt="avatar" /> 
    </div>

    <button class="signout-button" on:click={signout}>sign out</button>

    {:else}

      <h3>created using gun.js</h3>
  {/if}
</header>