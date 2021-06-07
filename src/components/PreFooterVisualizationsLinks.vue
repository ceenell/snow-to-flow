<template>
  <div class="pre-footer-links">
    <div class="inner-pre-footer-links-container">
      <p>See our other visualizations:</p>
      <div class="footer-viz-links">
        <a
          :href="LinkOne"
          target="_blank"
        >
          <figure>
            <img
              src="@/assets/components/PreFooterVisualizationsLinks/images/temp-monitor.jpg"
              alt=""
            >
            <figcaption>How we monitor stream temperature in the Delaware River Basin</figcaption>
          </figure>
        </a>
        <a
          :href="LinkTwo"
          target="_blank"
        >
          <figure>
            <img
              src="@/assets/components/PreFooterVisualizationsLinks/images/snow-to-flow.jpg"
              alt=""
            >
            <figcaption>From Snow to Flow</figcaption>
          </figure>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: 'PreFooterVisualizationsLinks',
        data() {
            return {
                LinkOne: process.env.VUE_APP_FOOTER_1,
                LinkTwo: process.env.VUE_APP_FOOTER_2
            };
        }
    }
</script>

<style scoped lang="scss">
$notWhite: white;
$nearBlack: #1a1b1c; 
/* for mobile */
#app {
  .pre-footer-links {
    display: flex;
    justify-content: center;
    text-align: center;
    font-family: 'Source Sans Pro',sans-serif;
    font-size: 16px;
    font-weight: 400;
    padding-top: .25em;
    p {
      color: $nearBlack;
      font-size: 1.3em;
    }
    background-color: $notWhite;

    .footer-viz-links {
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;

      img {
        width: 200px;
        height: 200px;
        top: 0;
        left: 0;
      }
      a {
        figcaption {
          color: $nearBlack;
          text-align: center;
          padding-bottom: 0.5em;
        }
        padding: 0.5em;
        max-width: 25rem;
      }
    }
  }
}

/* for everything but mobile */
@media only screen and (min-width: 700px) {
  #app {
    .pre-footer-links {
      .footer-viz-links {
        flex-direction: row;
        justify-content: center;
      }
    }
  }
}

#code-repository-link-container {
  a {
    color:$notWhite;
  }
}
</style>
