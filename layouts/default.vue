<template>
  <div id="main">
    <div class="headroom">
      <div class="navbar" role="navigation">
        <div class="navbar-brand">
          <nuxt-link to="/timeline" class="navbar-item" target="_new"
            ><img class="navbar-logo" src="~assets/techlabs-global-logo.svg" />
          </nuxt-link>
          <nuxt-link
            class="navbar-item techlabs-berlin-logo"
            to="/timeline"
            target="_new"
            ><img class="navbar-logo" src="~assets/techlabs-berlin-logo.svg" />
          </nuxt-link>

          <a
            role="button"
            class="navbar-burger burger"
            aria-label="menu"
            aria-expanded="false"
            data-target="navbar"
          >
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>
        <div id="navbar" class="navbar-menu">
          <div class="navbar-start">
            <nuxt-link
              to="/timeline"
              class="navbar-item has-text-centered is-tab"
              >Timeline</nuxt-link
            >
            <nuxt-link to="/faq" class="navbar-item has-text-centered is-tab"
              >FAQ</nuxt-link
            >
            <nuxt-link to="/media" class="navbar-item has-text-centered is-tab"
              >Media</nuxt-link
            >
          </div>
          <div class="navbar-end">
            <div class="navbar-item navbar-social-link">
              <a href="https://facebook.com/techlabsberlin" target="_new">
                <Fab i="facebook-f" />
                <span class="navbar-social-link-handle">techlabsberlin</span>
              </a>
            </div>
            <div class="navbar-item navbar-social-link">
              <a href="https://instagram.com/techlabs.berlin" target="_new">
                <Fab i="instagram" />
                <span class="navbar-social-link-handle">techlabs.berlin</span>
              </a>
            </div>
            <div class="navbar-item navbar-social-link">
              <a href="https://techlabsberlin.slack.com" target="_new">
                <Fab i="slack" />
                <span class="navbar-social-link-handle"
                  >techlabsberlin.slack.com</span
                >
              </a>
            </div>
            <div class="navbar-item has-text-centered">
              <a
                href="https://techlabs.org/location/Berlin"
                target="_new"
                class="techlabs-button"
              >
                <Fas i="link" />
                <span>techlabs.org</span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="main-content">
      <nuxt />
    </div>

    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          <strong>Semester Radar</strong> by
          <nuxt-link to="/contact">TechLabs Berlin e.V</nuxt-link>.<br />
          Source code is available on
          <a href="https://github.com/TechLabs-Berlin/radar" target="_new"
            >GitHub</a
          >
          licensed
          <a href="http://opensource.org/licenses/mit-license.php" target="_new"
            >MIT</a
          >.<br />
          <nuxt-link to="/contact">Contact</nuxt-link> &middot;
          <nuxt-link to="/newsletter">Newsletter</nuxt-link><br />
          <NotificationOptOut />
        </p>
      </div>
    </footer>
    <div class="filler" />

    <!-- simpleanalytics.com -->
    <script async defer src="https://nlytcs.bln.techlabs.org/app.js"></script>
    <noscript
      ><img src="https://nlytcs.bln.techlabs.org/image.gif" alt=""
    /></noscript>
  </div>
</template>

<script>
import Fab from '~/components/Fab.vue'
import Fas from '~/components/Fas.vue'
import NotificationOptOut from '~/components/NotificationOptOut'
import { initializeNavbar } from '~/assets/layout'

export default {
  components: {
    Fab,
    Fas,
    NotificationOptOut
  },
  mounted() {
    initializeNavbar()
  },
  head() {
    return {
      title: 'TechLabs Berlin Semester Radar'
    }
  }
}
</script>

<style lang="sass">
.techlabs-berlin-logo
  padding-left: 0
</style>
