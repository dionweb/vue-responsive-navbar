<template>
  <div id="app">
    <div class="nav">
      <div class="nav-logo">
        <a href>Website Name</a>
      </div>
      <div class="nav-links">
        <ul>
          <li>
            <a href>Home</a>
          </li>
          <li>
            <a href>News</a>
          </li>
          <li>
            <a href>Contact</a>
          </li>
          <li>
            <a href>About</a>
          </li>
        </ul>
      </div>
      <div class="burger" v-on:click="isOpen = !isOpen">
        <svg v-show="!isOpen" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
          <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
        </svg>
        <svg v-show="isOpen" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
          <path
            d="M10 8.586L2.929 1.515 1.515 2.929 8.586 10l-7.071 7.071 1.414 1.414L10 11.414l7.071 7.071 1.414-1.414L11.414 10l7.071-7.071-1.414-1.414L10 8.586z"
          />
        </svg>
      </div>
    </div>
    <div class="sidenav" v-bind:class="{ 'sidenavIsOpen-sidenav': isOpen }">
      <ul>
        <li>
          <a href>Home</a>
        </li>
        <li>
          <a href>News</a>
        </li>
        <li>
          <a href>Contact</a>
        </li>
        <li>
          <a href>About</a>
        </li>
      </ul>
    </div>
    <main v-on:click="isOpen=false" v-bind:class="{ 'sidenavIsOpen-main': isOpen }">
      <h3>Lorem Ipsum</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident autem repellat architecto. Fugiat
        animi quia laborum ullam, ut nobis consequuntur?
      </p>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Placeat culpa hic quae quaerat aliquam ad
        ducimus velit quas itaque harum laboriosam dolorum atque fuga exercitationem iure, illo ex qui similique
        sequi veniam dolor, deleniti delectus expedita officiis! Architecto, dignissimos vero?
      </p>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto porro itaque accusantium! Autem est
        cupiditate perspiciatis. Accusamus odit dolore quis enim? Laborum aperiam error ab ipsa nisi odio
        deleniti. Obcaecati rerum doloribus explicabo vero. Esse officia excepturi maiores quidem? Molestiae
        suscipit repellendus eos iste ratione, eum aliquam saepe ducimus ad, voluptate tempore amet laboriosam
        nihil, eligendi earum qui deserunt velit! Temporibus itaque maiores rem vel omnis. Necessitatibus
        perferendis nisi et eum iusto fuga eius repudiandae totam? Distinctio quae cupiditate aspernatur.
      </p>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sequi perferendis, distinctio asperiores vel
        itaque, commodi dolor, totam nihil nobis natus inventore. Laboriosam quos doloremque quo dolor saepe!
        Omnis accusantium voluptas assumenda exercitationem nam dicta maxime eaque deleniti ea aut, repellendus
        alias, rerum expedita est sit blanditiis ratione voluptate id repellat eius sed at a fugiat qui! Esse
        quis explicabo consectetur, reiciendis maiores ut repudiandae atque hic nulla vel voluptate eligendi qui
        at odio impedit voluptatem error nihil. Corporis, temporibus unde?
      </p>
      <h3>Lorem Ipsum</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident autem repellat architecto. Fugiat
        animi quia laborum ullam, ut nobis consequuntur?
      </p>
      <p>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Placeat culpa hic quae quaerat aliquam ad
        ducimus velit quas itaque harum laboriosam dolorum atque fuga exercitationem iure, illo ex qui similique
        sequi veniam dolor, deleniti delectus expedita officiis! Architecto, dignissimos vero?
      </p>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Iusto porro itaque accusantium! Autem est
        cupiditate perspiciatis. Accusamus odit dolore quis enim? Laborum aperiam error ab ipsa nisi odio
        deleniti. Obcaecati rerum doloribus explicabo vero. Esse officia excepturi maiores quidem? Molestiae
        suscipit repellendus eos iste ratione, eum aliquam saepe ducimus ad, voluptate tempore amet laboriosam
        nihil, eligendi earum qui deserunt velit! Temporibus itaque maiores rem vel omnis. Necessitatibus
        perferendis nisi et eum iusto fuga eius repudiandae totam? Distinctio quae cupiditate aspernatur.
      </p>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Sequi perferendis, distinctio asperiores vel
        itaque, commodi dolor, totam nihil nobis natus inventore. Laboriosam quos doloremque quo dolor saepe!
        Omnis accusantium voluptas assumenda exercitationem nam dicta maxime eaque deleniti ea aut, repellendus
        alias, rerum expedita est sit blanditiis ratione voluptate id repellat eius sed at a fugiat qui! Esse
        quis explicabo consectetur, reiciendis maiores ut repudiandae atque hic nulla vel voluptate eligendi qui
        at odio impedit voluptatem error nihil. Corporis, temporibus unde?
      </p>
    </main>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      isOpen: false
    };
  }
};
</script>

<style>
body {
  margin: 0;
  min-height: 100vh;
  background: #22252c;
  font-family: "Lato", sans-serif;
}

a {
  text-decoration: none;
  color: #3498db;
  font-size: 1.1rem;
}

ul {
  list-style: none;
  text-align: center;
  padding: 0;
}

.nav {
  z-index: 2;
  height: 50px;
  background: #1b1d24;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 40px;
}

.nav .nav-links ul {
  display: inline-flex;
}

.nav .nav-links a {
  padding: 0 10px;
}

.burger {
  display: none;
  cursor: pointer;
}

.burger svg {
  fill: #3498db;
  height: 21px;
}

.sidenav {
  display: none;
  z-index: 2;
  height: calc(100vh - 70px);
  background-color: #1b1d24;
  width: 250px;
  margin-right: -250px;
  position: fixed;
  top: 70px;
  right: 0;
  transition: 0.4s;
}

.sidenav ul li {
  padding: 5px;
}

main {
  transition: 0.4s;
  color: #d4d7d7;
  margin-top: 40px;
  padding: 50px 40px 10px 40px;
}

.sidenavIsOpen-sidenav {
  margin-right: 0;
  transition: 0.4s;
}

.sidenavIsOpen-main {
  opacity: 0.2;
  transition: 0.4s;
}

@media only screen and (max-width: 550px) {
  .burger {
    display: block;
  }

  .nav-links {
    display: none;
  }

  .sidenav {
    display: block;
  }
}
</style>
