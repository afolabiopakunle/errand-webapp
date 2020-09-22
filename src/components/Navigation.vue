<template>
  <div>
    <nav class="site-nav navbar navbar-expand bg-primary navbar-dark">
      <div class="container-fluid">
        <router-link to="/" class="navbar-brand">Meeting Log</router-link>
        <div class="navbar-nav ml-auto">
          <router-link to="/meetings" class="nav-item nav-link text-white">Meetings</router-link>
          <router-link to="/login" class="nav-item nav-link text-white">Log in</router-link>
          <router-link to="/register" class="nav-item nav-link text-white">Register</router-link>
        </div>
      </div>
    </nav>
  </div>
</template>