<script setup>
useHead({
  script: [
    {
      src: 'https://cdn.tailwindcss.com',
      body: true
    }
  ]
})
</script>

<template>
   <div class="content">
      <Navbar />
      <slot></slot>
   </div> 
    <div class="footer">
      <TheFooter />
    </div>
</template>

<style>
/* Скрываем Scrollbar */
body {
	scrollbar-width: none; /* Firefox */
}
body::-webkit-scrollbar { 
	display: none; /* Safari and Chrome */
}

 body {
  /* margin: 0;
	padding: 0; */
	color: #fff;
  font-family: 'Roboto Mono', monospace;
  font-size: 16px;
  line-height: 24px;
  font-weight: 400;
  letter-spacing: 0.05em;
  text-align: center;
  background-color: #000000;
  height: 100%;
}
.content {
  min-height: 100%;
  padding-bottom: 50px;
  }
  .footer {
  height: 40px;
  margin-top: -40px;
  }

.tracking-in-contract-bck {
  animation: tracking-in-contract-bck 2s cubic-bezier(.215, .61, .355, 1.000) both
}

@keyframes tracking-in-contract-bck {
  0% {
    letter-spacing: 1em;
    transform: translateZ(400px);
    opacity: 0
  }

  40% {
    opacity: .6
  }

  100% {
    transform: translateZ(0);
    opacity: 1
  }
}
/* Contact */
.backInRight {
  animation: 3s linear 250ms backwards running backInRight;
}

@keyframes backInRight {
  0% {
    transform: translateX(2000px) scale(0.7);
    opacity: 0.7;
  }

  80% {
    transform: translateX(0px) scale(0.7);
    opacity: 0.7;
  }

  100% {
    transform: scale(1);
    opacity: 1;
  }
}

.backInLeft {
  animation: 3s linear 250ms backwards alternate backInLeft;
}
@keyframes backInLeft {
  0% {
    transform: translateX(-2000px) scale(0.7);
    opacity: 0.7;
  }

  80% {
    transform: translateX(0px) scale(0.7);
    opacity: 0.7;
  }

  100% {
    transform: scale(1);
    opacity: 1;
  }
}

.bounceInUp {
  animation: 3s linear bounceInUp;
}
@keyframes bounceInUp {
  from,
  60%,
  75%,
  90%,
  to {
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }

  from {
    opacity: 0;
    transform: translate3d(0, 3000px, 0) scaleY(5);
  }

  60% {
    opacity: 1;
    transform: translate3d(0, -20px, 0) scaleY(0.9);
  }

  75% {
    transform: translate3d(0, 10px, 0) scaleY(0.95);
  }

  90% {
    transform: translate3d(0, -5px, 0) scaleY(0.985);
  }

  to {
    transform: translate3d(0, 0, 0);
  }
}

.backInUp {
  animation: 3s linear backwards running backInUp;
}
@keyframes backInUp {
  0% {
    transform: translateY(1200px) scale(0.7);
    opacity: 0.7;
  }

  80% {
    transform: translateY(0px) scale(0.7);
    opacity: 0.7;
  }

  100% {
    transform: scale(1);
    opacity: 1;
  }
}

/* Home */
.roll-in-left {
    animation: roll-in-left 2s ease-out both
}
@keyframes roll-in-left {
    0% {
        transform: translateX(-800px) rotate(-540deg);
        opacity: 0
    }

    100% {
        transform: translateX(0) rotate(0deg);
        opacity: 1
    }
}

.jello-vertical {
  animation: jello-vertical 2s 4s both
}
@keyframes jello-vertical {
  0% {
    transform: scale3d(1, 1, 1)
  }

  30% {
    transform: scale3d(.75, 1.25, 1)
  }

  40% {
    transform: scale3d(1.25, .75, 1)
  }

  50% {
    transform: scale3d(.85, 1.15, 1)
  }

  65% {
    transform: scale3d(1.05, .95, 1)
  }

  75% {
    transform: scale3d(.95, 1.05, 1)
  }

  100% {
    transform: scale3d(1, 1, 1)
  }
}

.roll-in-right {
    animation: roll-in-right 2s ease-out 2s both
}
@keyframes roll-in-right {
    0% {
        transform: translateX(800px) rotate(540deg);
        opacity: 0
    }

    100% {
        transform: translateX(0) rotate(0deg);
        opacity: 1
    }
}
</style>
