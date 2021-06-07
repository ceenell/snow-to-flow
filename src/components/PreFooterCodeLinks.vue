<template>
  <div id="code-repository-link-container">
    <a
      :href="gitHubRepositoryLink"
      target="_blank"
      aria-label="github link"
    >Get the {{ projectTitle }} code
      <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'github' }" />
    </a>
  </div>
</template>

<script>
  export default {
      name: 'PreFooterCodeLinks',
      data() {
          return {
              gitHubRepositoryLink: process.env.VUE_APP_GITHUB_REPOSITORY_LINK,
              projectTitle: process.env.VUE_APP_TITLE
          }
      }
  }

</script>

<style lang="scss">
$nearBlack: #1a1b1c; 
  #code-repository-link-container {
    display: flex;
    justify-content: center;
    width: 100%;
    background-color: #c2c4c5;
    margin: 0 auto;
    padding-bottom: 0.4rem;
    a {
      color: #090211;
      font-family: 'Source Sans Pro',sans-serif;
      text-decoration: none
    }
  }

</style>
