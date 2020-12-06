<template>
  <div class="app-container">
    <div class="app-header">
      <div class="app-header__status-bar">
        <div class="app-header__clock">9:41</div>
        <div class="app-header__sensors">
          <div class="device__cellular">
            <img src="@/assets/svg/device-cellular.svg" alt="cellular-logo" />
          </div>
          <div class="device__wifi">
            <img src="@/assets/svg/device-wifi.svg" alt="wifi-logo" />
          </div>
          <div class="device__battery">
            <img src="@/assets/svg/device-battery.svg" alt="battery-logo" />
          </div>
        </div>
      </div>
      <div class="app-header__navigation">
        <div class="app-header__menu">
          <img src="@/assets/svg/app-menu.svg" alt="logo" />
        </div>
        <div class="app-header__logo">
          <img src="@/assets/svg/app-logo.svg" alt="logo" />
        </div>
        <div class="app-header__cart">
          <img src="@/assets/svg/app-cart.svg" alt="logo" />
        </div>
      </div>
    </div>
    <div class="app__main">
      <div class="app__main-container">
        <div class="app__main-slider">Banner</div>
        <div class="app__main-categories">Categories</div>
        <div class="app__main-section">Recomendations</div>
        <div class="app__main-section">Promotions</div>
        <div class="app__main-section">Promotions</div>
      </div>
    </div>
    <div class="app__footer">
      <div class="top-menu-container">
        <div class="top-menu__button">
          <div class="top-menu__button-container">
            <img src="@/assets/svg/navigation-search.svg" alt="search-icon" />
          </div>
        </div>
        <div class="top-menu__subtract">
          <div class="top-menu__navigation">
            <div class="top-menu__navigation-right">
              <div class="user-on">
                <img src="@/assets/svg/app-home.svg" alt="home-icon" />
              </div>
              <div class="user-favourites">
                <img
                  src="@/assets/svg/app-favorites.svg"
                  alt="favorites-icon"
                />
              </div>
            </div>
            <div class="top-menu__navigation-left">
              <div class="user-message">
                <img src="@/assets/svg/app-messages.svg" alt="messages-icon" />
              </div>
              <div class="user-home">
                <img src="@/assets/svg/app-user.svg" alt="user-icon" />
              </div>
            </div>
          </div>
          <div class="top-menu__home-indicator">
            <div class="home-indicator">
              <img
                src="@/assets/svg/device-home-indicator.svg"
                alt="home-indicator"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "Home",
  data: () => ({})
});
</script>

<style lang="scss" scoped>
.app {
  &-container {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    justify-content: space-between;
  }
  &-header {
    position: fixed;
    top: 0;
    min-width: 100%;
    min-height: 105px;
    &__navigation {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      padding: 17px 27px 20px;
      > div {
        cursor: pointer;
        > img {
          display: block;
        }
      }
    }
    &__clock {
      margin-left: 33px;
      font-weight: 600;
      font-size: 14px;
    }
    &__status-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 14px 0 13px;
    }
    &__sensors {
      display: flex;
      margin-right: 14px;
      & > div {
        > img {
          display: block;
        }
        &:not(:last-of-type) {
          margin-right: 5px;
        }
      }
    }
  }
  &__footer {
    position: fixed;
    min-width: 100%;
    bottom: 0;
    .top-menu {
      &-container {
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }
      &__home-indicator {
        padding: 21px 0 8px;
        .home-indicator {
          img {
            display: block;
            margin: auto;
          }
        }
      }
      &__subtract {
        min-height: 92px;
        background-image: url("../assets/svg/app-footer-background.svg");
        padding-top: 10px;
      }
      &__navigation {
        display: flex;
        justify-content: space-between;
        padding: 24px 40px 0;
        align-items: center;
        &-right,
        &-left {
          display: flex;
          justify-content: space-between;
          align-items: center;
          > div {
            cursor: pointer;
            &:not(:last-of-type) {
              margin-right: 46px;
            }
            > img {
              display: block;
            }
          }
        }
      }
      &__button {
        position: fixed;
        bottom: 55px;
        left: 50%;
        transform: translateX(-50%);
        &-container {
          cursor: pointer;
          background: #00d173;
          width: 54px;
          height: 54px;
          display: flex;
          justify-content: center;
          align-items: center;
          border-radius: 50%;
          margin: auto;
        }
      }
    }
  }
  &__main {
    min-height: 100vh;
    &-container {
      height: 100%;
      padding: 15px;
      margin: 105px 0 82px;
    }
  }
}
</style>
