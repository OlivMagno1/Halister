<template>
  <div class="wrapper">
    <svg
      preserveAspectRatio=none
      viewBox="0 0 100 100"
    >
      <path
        :fill=backColor
        d="
          M 0,0 
          L 93.28,0 96.43,19.25 90.13,59.62 0,93.9
          z"
      />
    </svg>
    <span :style="{'color':fontColor}">{{ string }}</span>
  </div>
</template>

<script>
export default {
  props: ['string', 'fontColor', 'backColor', 'shadeColor'],
};
</script>

<style scoped>
.wrapper {
  position: relative;
  
}

svg {
  position: absolute;
}

span {
  font-family: BebasNeue, sans-serif;
  text-transform: uppercase;
  
  position: absolute;
  cursor: default;
}

@media (width < 1000px) {
  .wrapper {
    top: clamp(1rem, -0.88rem + 9.4vw, 5rem);
    margin-bottom: 1rem;
    height: clamp(3rem, -0.59rem + 18vw, 10.625rem);
  }
  
  svg {
    height: clamp(3rem, -0.59rem + 18vw, 10.625rem);
    width: clamp(8rem, 0.306rem + 38vw, 24.35rem);
  }

  span {
    font-size: clamp(0.9rem, 0.28rem + 2.75vw, 2rem);
    padding:
      clamp(0.25rem, -0.57rem + 4vw, 2rem)
      clamp(0rem, -0.47rem + 2vw, 1rem)
      clamp(0rem, -0.71rem + 3.5vw, 1.5rem)
      clamp(0.5rem, -0.69rem + 6vw, 3rem);
  }
}

@media (width >= 1000px) {
  .wrapper {
    top: 5rem;
    margin-bottom: 5rem;
    height: 10.7rem;
  }

  svg {
    height: 10.625rem;
    width: 24.35rem;
  }

  span {
    font-size: 3rem;
    padding: 2rem 1rem 1.5rem 3rem;
  }

}
</style>