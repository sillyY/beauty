<template>
    <button class="c-btn c-btn__1">
      <span>Read More</span>
    </button>
</template>
<script>
export default {
  name: "Animation-button",
  data() {
    return {};
  },
};
</script>
<style lang="scss" scoped>
.c-btn {
  position: relative;
  display: inline-block;
  transition: all 0.3s ease;
  box-shadow: inset 2px 2px 2px 0px rgba(255, 255, 255, 0.5),
    7px 7px 20px 0px rgba(0, 0, 0, 0.1), 4px 4px 5px 0px rgba(0, 0, 0, 0.1);
  outline: none;
  width: 130px;
  height: 40px;
  padding: 10px 25px;
  border-radius: 5px;
  background-color: transparent;
  font-family: "Lato", sans-serif;
  font-weight: 500;
  color: #fff;
  line-height: 42px;
  cursor: pointer;
  &__1 {
    background: linear-gradient(
      0deg,
      rgba(0, 172, 238, 1) 0%,
      rgba(2, 126, 251, 1) 100%
    );
    width: 130px;
    height: 40px;
    line-height: 42px;
    padding: 0;
    border: none;
    &::before,
    &::after {
      position: absolute;
      content: "";
      right: 0;
      top: 0;
      background: rgba(2, 126, 251, 1);
      transition: all 0.3s ease;
    }
    &::before {
      width: 2px;
      height: 0;
    }
    &::after {
      width: 0;
      height: 2px;
    }
    &:hover {
      background: transparent;
      box-shadow: none;
      &::before {
        height: 100%;
      }
      &::after {
        width: 100%;
      }
    }

    & > span {
      position: relative;
      display: block;
      width: 100%;
      height: 100%;
      &::before,
      &::after {
        position: absolute;
        content: "";
        left: 0;
        bottom: 0;
        background: rgba(2, 126, 251, 1);
        transition: all 0.3s ease;
      }
      &::before {
        width: 2px;
        height: 0%;
      }
      &::after {
        width: 0%;
        height: 2px;
      }
      &:hover {
        color: rgba(2, 126, 251, 1);
        &::before {
          height: 100%;
        }
        &::after {
          width: 100%;
        }
      }
    }
  }
}
</style>