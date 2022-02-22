<template>
        <nav class="navbar fixed-top navbar-light app-background">
      <div class="container-fluid">
        <a class="navbar-brand dynamic-title" href="#">TRIE</a>
        <div class="d-flex">
          <div v-if="lightMode">
            <span class="material-icons-outlined">
            beach_access
            </span>
            <span v-on:click='ToggleSwitch' class="material-icons-outlined theme-switch">
              toggle_off
            </span>
          </div>
          <div v-else>
            <span class="material-icons text-warning">
            emoji_objects
            </span>
            <span v-on:click='ToggleSwitch' class="material-icons text-light theme-switch">
            toggle_on
            </span>
          </div>
        </div>
      </div>
    </nav>
</template>

<script>
export default {
    name: 'AppBar',
    data: function() {
return {
      lightMode: true,
    };
    
},
   mounted() {
    document.title = 'Project 1'

    let bodyElement = document.body
    bodyElement.classList.add("app-background")

    let htmlElement = document.documentElement
    let theme = localStorage.getItem("theme");

    if(theme === 'dark') {
      htmlElement.setAttribute('theme', 'dark')
      this.lightMode = false
    }else {
      htmlElement.setAttribute('theme', 'light')
      this.lightMode = true
    }
  },
  methods: {
    ToggleSwitch() {
      if(this.lightMode === true){
        this.lightMode = false
      } else {
        this.lightMode = true
      }
    }
  },
  watch: {
    lightMode: function () {
      let htmlElement = document.documentElement;
      if (this.lightMode) {
        localStorage.setItem("theme", 'light'),
        htmlElement.setAttribute('theme', 'light');
      }else {
        localStorage.setItem("theme", "dark");
        htmlElement.setAttribute("theme", 'dark');
      }
    }
  }
}
</script>