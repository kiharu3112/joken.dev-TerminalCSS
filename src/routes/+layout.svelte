<script>
  import 'terminal.css'
  import { page } from '$app/stores'
</script>
<header>
  <a href="/" class="link">NITMC JOKEN</a>
</header>

<div id="body">
  <div id="pwd">
    <p class="code">pwd</p>
    <div class="pwd-result">
      <a href="/">/</a>
      {#if $page.url.pathname === "/achievements"}
      <a href="/achievements">achievements</a>
      {/if}
      {#if $page.url.pathname === "/members"}
      <a href="/members">Members</a>
      {/if}
      {#if $page.url.pathname === "/activity"}
      <a href="/activity">Activities</a>
      {/if}
      {#if $page.url.pathname === "/works"}
      <a href="/works">Contact</a>
      {/if}
      {#if $page.url.pathname === "/join"}
      <a href="/join">Join</a>
      {/if}
    </div>
  </div>
  <div id="ls">
    <p class="code">ls /</p>
    <div class="ls-result">
      <a href="/achievements">achievements</a>
      <a href="/members">members</a>
      <a href="/activity">activity</a>
      <a href="/works">works</a>
      <a href="/join">join</a>
      <a href="https://joken.dev">joken.dev</a>
    </div>
  </div>
  <slot />
</div>
<style>
  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 800px;
    margin: 0 auto;
    padding-top: 0.3rem;
  }
  a {
    margin-right: 0.5rem;
  }
  .link {
    font-size: 1rem;
    font-weight: 600;
    margin: 0;
    padding: 0;
  }
  .link::before {
    content: '> ';
  }
  .code {
    color: #287100;
    margin: 0;
  }
  .code::before {
    content: '$ ';
    color: #000000
  }
  .pwd-result {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    margin-bottom: 1rem;
  }
  #body {
    max-width: 800px;
    margin: 0 auto;
    padding: 1rem 0;
  }
</style>