<template>
  <div id="app">
    <div class="top-spacer">
      <div class="typewriter">
        <h1>eru123.github.io</h1>
      </div>
    </div>
    <div id="nav">
      <div class="jumbotron">
        <div class="actions">
          <router-link to="/">Developer</router-link>
          <router-link to="/projects">Projects</router-link>
        </div>
      </div>
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
body {
  box-sizing: border-box;
  margin: 0;
}
* {
  user-select: none;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  position: sticky;
  top: 0;
}
.top-spacer {
  background: url("assets/bg-top.png");
  height: 60vh;
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;

  .typewriter h1 {
    color: #fff;
    text-shadow: 1px 5px 5px #333;
    overflow: hidden; /* Ensures the content is not revealed until the animation */
    border-right: 0.15em solid orange; /* The typwriter cursor */
    white-space: nowrap; /* Keeps the content on a single line */
    margin: 0 auto; /* Gives that scrolling effect as the typing happens */
    letter-spacing: 0.15em; /* Adjust as needed */
    animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
  }

  /* The typing effect */
  @keyframes typing {
    from {
      width: 0;
    }
    to {
      width: 100%;
    }
  }

  /* The typewriter cursor effect */
  @keyframes blink-caret {
    from,
    to {
      border-color: transparent;
    }
    50% {
      border-color: orange;
    }
  }
}
.jumbotron {
  background: #008ae6;
  padding: 20px 0;
  display: flex;
  justify-content: center;
  .actions {
    a {
      display: inline-block;
      font-weight: bold;
      color: #2c3e50;
      padding: 10px 20px;
      background: rgba($color: #fff, $alpha: 0.6);
      text-decoration: none;
      margin: 0 5px;
      transition: 0.2s;
      border-radius: 20px;
      &:hover {
        background: rgba($color: #fff, $alpha: 0.9);
      }
      &.router-link-exact-active {
        background: rgba($color: #3dda96, $alpha: 1);
      }
    }
  }
}
</style>
