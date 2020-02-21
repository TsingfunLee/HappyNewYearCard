<template>
  <div id="index-wrap">
    <div class="bg-img fu"></div>
    <div class="text-container">
      <div class="two num bg-img"></div>
      <div class="zero num bg-img"></div>
      <div class="two num bg-img"></div>
      <div class="zero num bg-img"></div>
    </div>
    <div class="bg-img happy"></div>
    <div class="type-text">
      <span>新年快乐</span>
    </div>
    <div class="touch" v-if="false"></div>
    <div class="bg-img bottom"></div>
    <a href="https://github.com/TsingfunLee" class="link">@TsingfunLee/池月</a>
  </div>
</template>

<script>
export default {
  name: "index",
  components: {}
};
</script>

<style lang="scss" scoped>
#index-wrap {
  padding-top: 2.34rem;
  height: 100%;
  position: absolute;
  left: 50%;
  top: 0;
  transform: translateX(-50%);
  background-color: #6f9d5c;
  box-sizing: border-box;
  @media (min-aspect-ratio : 768/1024){
    min-height: 12.06rem;
  }
  &::before {
    content: "";
    display: block;
    background-image: url(../assets/pattern.png);
    background-size: contain;
    background-repeat: no-repeat;
    width: 4.7rem;
    height: 3.3rem;
    position: absolute;
    top: 0;
    right: 0;
    animation: twinkle 8s ease-in 3s alternate infinite both;
  }
  &::after {
    content: "";
    display: block;
    background-image: url(../assets/corner.png);
    background-size: contain;
    background-repeat: no-repeat;
    width: 0.74rem;
    height: 0.74rem;
    position: absolute;
    right: 0;
    bottom: 0;
  }
  .fu {
    background-image: url(../assets/fu.png);
    width: 0.98rem;
    height: 0.92rem;
    position: relative;
    margin: 0 auto;
  }
  .text-container {
    margin: 0.36rem 0 0.4rem 0;
    display: flex;
    padding: 0 0.79rem;
    .num {
      width: 1.48rem;
      height: 1.8rem;
      animation: rolling 0.8s linear normal 1 both;
      &:nth-child(1) {
        animation-delay: 0;
      }
      &:nth-child(2) {
        animation-delay: 1s;
      }
      &:nth-child(3) {
        animation-delay: 2s;
      }
      &:nth-child(4) {
        animation-delay: 3s;
      }
      &.two {
        background-image: url(../assets/2.png);
      }
      &.zero {
        background-image: url(../assets/0.png);
      }
    }
  }
  .happy {
    width: 7.5rem;
    height: 0.68rem;
    background-image: url(../assets/happynewyear.png);
    animation: bounceInDown 1s ease 3.8s both;
  }
  .type-text {
    color: #a71616;
    font-size: 0.72rem;
    line-height: 1;
    margin-top: 0.44rem;
    width: 4em;
    position: relative;
    white-space: nowrap;
    left: 50%;
    transform: translateX(-50%);
    span{
      white-space: nowrap;
      overflow: hidden;
      display: inline-block;
      animation: typing 2s steps(1) 4.8s both;
    }
    &::after {
      content: "";
      display: inline-block;
      width: 1px;
      height: 0.72rem;
      background-color: #a71616;
      vertical-align: top;
      margin-left: 0.12rem;
      animation: cursor 0.4s linear 4.8s both infinite;
    }
  }
  .touch{
    width: 0.8rem;
    height: 0.8rem;
    border-radius: 100%;
    border: solid #e2ff89 0.08rem;
    margin: 0.8rem auto 0 auto;
    animation: scale 1s ease 6.8s alternate both infinite;
  }
  .bottom {
    background-image: url(../assets/bottom.png);
    width: 2.64rem;
    height: 1.04rem;
    position: absolute;
    bottom: 0.62rem;
    left: 50%;
    margin-left: -1.32rem;
  }
  .link {
    font-size: 0.18rem;
    color: #e2ff89;
    position: absolute;
    bottom: 0.22rem;
    left: 50%;
    transform: translateX(-50%);
    &:focus {
      outline: none;
    }
  }
}

@keyframes twinkle {
  0% {
    opacity: 0;
  }
  30%{
    opacity: 0;
  }
  80% {
    opacity: 0.75;
  }
}

@keyframes rolling {
  from {
    transform: rotateX(90deg);
  }
  to {
    transform: rotateX(0);
  }
}
@keyframes bounceInDown {
  0% {
    opacity: 0;
    transform: translateY(-1rem);
  }
  60% {
    opacity: 1;
    transform: translateY(0.3rem);
  }
  80% {
    transform: translateY(-0.3rem);
  }
  100% {
    transform: translateY(0);
  }
}
@keyframes cursor {
  from{
    opacity: 0;
  }
  to{
    opacity: 1;
  }
}
@keyframes typing {
  0%{
    width: 0;
  }
  25%{
    width: 1em;
  }
  50%{
    width: 2em;
  }
  75%{
    width: 3em;
  }
  100%{
    width: 4em;
  }
}
@keyframes scale{
  from{
    transform: scale(0.6, 0.6);
  }
  to{
    transform: scale(1, 1);
  }
}
</style>
