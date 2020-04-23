<script>
  export let nickname;
  export let name;
</script>

<style>
  .Profile-content {
    display: flex;
    align-items: center;
  }

  .Profile-avatar img {
    width: 42px;
    height: 42px;
    border-radius: 50%;
  }

  .Profile-info {
    margin: 0 0 0 0.5em;
  }

  .Profile-info h2 {
    font-size: 14px;
    color: black;
    margin: 0;
    padding: 0;
  }

  .Profile-info span {
    font-size: 12px;
    font-weight: normal;
  }
</style>

<div class="Profile">
  <div class="Profile-content">
    <div class="Profile-avatar"><img
        src="https://avatars1.githubusercontent.com/u/24970023?s=60&u=84aaf62be9d8f48b8a58b6934123ef75ed67d237&v=4"
        alt=""></div>
  </div>
  <div class="Profile-info">
    <h2>{nickname}</h2>
    <span>{name}</span>
  </div>
</div>
