<template>
  <input type="checkbox" class="c-checkbox" />
</template>
<script>
export default {
  name: "Checkbox",
  data() {
    return {};
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
input[type="checkbox"] {
  position: relative;
  background: #36d9d8;
  border: none;
  transition: 0.3s;
}
input {
  outline: 0;
  appearance: none;
}
.c-checkbox {
  width: 24px;
  height: 24px;
  border-radius: 50%;
  cursor: pointer;
  outline: none;
  &:hover {
    border-color: #85919f;
  }
  &:checked {
        @-webkit-keyframes scale-in {
      to {
        transform: scale(1);
      }
    }

    @keyframes scale-in {
      to {
        transform: scale(1);
      }
    }
    &::before {
      -webkit-animation: scale-in 0.1s 0.2s linear forwards;
      animation: scale-in 0.1s 0.2s linear forwards;
    }
    &::after {
      transform: scale(0);
    }
  }
  &::before {
    top: 1px;
    width: 24px;
    height: 24px;
    display: flex;
    justify-content: center;
    align-items: center;
    line-height: 1;
    position: absolute;
    content: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='18px' height='18px' fill='none' stroke-width='2px' stroke='white' stroke-linecap='round' viewBox='0 0 21 21'%3E%3Cpolyline points='5 10.75 8.5 14.25 16 6'%3E%3C/polyline%3E%3C/svg%3E");
    transform: scale(0);
  }
  &::after {
    position: absolute;
    content: "";
    width: 100%;
    height: 100%;
    background: white;
    border-radius: inherit;
    box-shadow: inset 0 0 0 1px #cdd2da;
    transition: 0.2s;
  }
}
</style>