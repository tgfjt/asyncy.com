<template>
  <section class="problem">
    <a-card>
      <div
        slot="head"
        class="head-problem">
        <h2 class="is-size-2 has-text-dark">Applications are <b>stories of data.</b></h2>
        <h5 class="is-size-5 has-text-gray-2">Create a Slack bot that replies with the weather forecast.</h5>
      </div>
      <svg
        class="dots-separator"
        width="100%"
        height="12px"
        viewBox="0 0 886 12"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <g
          stroke="none"
          stroke-width="1"
          fill="none"
          fill-rule="evenodd">
          <g
            transform="translate(1, 1)"
            fill-rule="nonzero">
            <path
              d="M2.5,5.09347003 L879.688787,5.09347003"
              stroke="#C6C7DC"
              stroke-linecap="round"
              stroke-dasharray="4 6"
            />
            <circle
              stroke="#5805FC"
              stroke-width="2"
              fill="#5805FC"
              cx="879"
              cy="5"
              r="5"/>
            <circle
              stroke="#5805FC"
              stroke-width="2"
              fill="#F2F3F9"
              cx="5"
              cy="5"
              r="5"/>
            <circle
              stroke="#5805FC"
              stroke-width="2"
              fill="#AFA3C8"
              cx="295"
              cy="5"
              r="5"/>
            <circle
              stroke="#5805FC"
              stroke-width="2"
              fill="#8367BB"
              cx="585"
              cy="5"
              r="5"/>
          </g>
        </g>
      </svg>
      <div class="columns is-centered step-cards-container">
        <div class="column is-one-quarter">
          <div class="step-card">
            <div class="picture slack-bot"/>
            <div class="what">create a slack bot</div>
          </div>
        </div>
        <div class="column is-one-quarter">
          <div class="step-card">
            <div class="picture neural-network"/>
            <div class="what">neural network</div>
          </div>
        </div>
        <div class="column is-one-quarter">
          <div class="step-card">
            <div class="picture accuweather"/>
            <div class="what">accuweather</div>
          </div>
        </div>
        <div class="column is-one-quarter">
          <div class="step-card">
            <div class="picture send-reply"/>
            <div class="what">send reply</div>
          </div>
        </div>
      </div>
    </a-card>
    <div class="container">
      <div class="columns is-centered text--left separated">
        <div class="column is-full">
          <div class="container">
            <h5 class="is-size-5 has-text-gray-2">
              It's 2019; software development is still
              <br>riddled with <b>unnecessary complexity</b> and <b>poor reusability.</b>
            </h5>
          </div>
          <div class="complexity"/>
          <h5 class="is-size-5 has-text-gray-2">
            Time to <b>drop the complexity</b> and <b>amplify the story of data</b>
            <br>by designing service-oriented, fully-asynchronous applications.
          </h5>
          <a-boxed class="boxed">
            <h3 class="is-size-3 has-text-dark has-text-centered">
              We need a language for <b>data storytelling.</b>
            </h3>
          </a-boxed>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Problem'
}
</script>

<style lang="scss" scoped>
@import "~bulma/sass/utilities/mixins";

.problem {
  padding: 3rem 0;
  @include mobile {
    padding: 0;
  }

  .separated { margin-top: 9.25rem }
  .columns {
    h5 {
      margin: 1rem 10rem;
      @include touch {
        margin: 1rem 3rem;
      }
    }
  }

  .head-problem { max-width: 1130px; margin: 0 auto }

  .dots-separator {
    margin: 5rem 0 2rem;
    position: relative;
  }

  .boxed {
    @include desktop {
      margin-top: 3rem;
      margin-bottom: 5rem;
    }
  }

  .complexity {
    margin: 5rem 0;
    @include touch {
      margin: 0;
    }
    height: 550px;
    @include mobile {
      height: 300px;
    }
    width: 100%;
    background-size: contain;
    background-image: url("~@/assets/img/complexity.svg");
    background-repeat: no-repeat;
    background-position: center center;
  }

  .step-cards-container {
    max-width: 1060px;
    margin: 0 auto;
    padding: 0;
  }

  .step-card {
    background-color: $white;
    border-radius: 0.5rem;
    display: flex;
    height: 250px;
    width: 100%;
    max-width: 250px;
    padding: 0;
    flex-direction: column;
    margin: 0;

    div {
      flex-grow: 0;
      width: 100%;
      padding: 0.5rem;
      text-align: center;
      margin: auto;
    }
    div + div {
      border-top: 1px solid $light;
    }
  }

  .picture {
    flex: 1 1 100%;
    width: 8rem;
    height: auto;
    background-position: center;
    background-repeat: no-repeat;
    background-size: contain;
    &.slack-bot {
      background-image: url("~@/assets/img/slack-bot.svg");
    }
    &.neural-network {
      background-image: url("~@/assets/img/neural-network.svg");
    }
    &.accuweather {
      background-image: url("~@/assets/img/accuweather.svg");
    }
    &.send-reply {
      background-image: url("~@/assets/img/send-reply.svg");
    }
  }

  .what {
    flex: 0 0 auto;
    margin-top: 2.5rem;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 1rem;
    letter-spacing: 0.01rem;
    color: nth($grays, 2);
  }
}
</style>
