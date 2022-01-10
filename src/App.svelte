<script lang="ts">
  import { Parallax, ParallaxLayer } from "svelte-parallax";

  let parallax;
  let disabled = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

  const icon = () => "/icon.gif";
</script>

<Parallax
  sections="3"
  style="background-color: #070c0c;"
  {disabled}
  bind:this={parallax}
>
  <ParallaxLayer offset="1" rate="1" style="background-color: #02023d;" />
  <ParallaxLayer offset="2" rate="1" style="background-color: #7f5504;" />

  <ParallaxLayer offset="1" rate="0.8" style="opacity: 0.1;">
    <img
      src={icon()}
      alt=""
      style="display: block; width: 20%; margin-left: 55%; border-radius: 100px;"
    />
    <img
      src={icon()}
      alt=""
      style="display: block; width: 10%; margin-left: 15%; border-radius: 100px;"
    />
  </ParallaxLayer>

  <ParallaxLayer offset="1.75" rate="0.5" style="opacity: 0.1;">
    <img
      src={icon()}
      alt=""
      style="display: block; width: 20%; margin-left: 70%; border-radius: 100px;"
    />
    <img
      src={icon()}
      alt=""
      style="display: block; width: 20%; margin-left: 40%; border-radius: 100px;"
    />
  </ParallaxLayer>

  <ParallaxLayer offset="1" rate="0.2" style="opacity: 0.2;">
    <img
      src={icon()}
      alt=""
      style="display: block; width: 10%; margin-left: 10%; border-radius: 100px;"
    />
    <img
      src={icon()}
      alt=""
      style="display: block; width: 20%; margin-left: 75%; border-radius: 100px;"
    />
  </ParallaxLayer>

  <ParallaxLayer offset="1.6" rate="-0.1" style="opacity: 0.4;">
    <img
      src={icon()}
      alt=""
      style="display: block; width: 20%; margin-left: 60%; border-radius: 100px;"
    />
    <img
      src={icon()}
      alt=""
      style="display: block; width: 25%; margin-left: 30%; border-radius: 100px;"
    />
    <img
      src={icon()}
      alt=""
      style="display: block; width: 10%; margin-left: 80%; border-radius: 100px;"
    />
  </ParallaxLayer>

  <ParallaxLayer offset="2.6" rate="0.4" style="opacity: 0.6;">
    <img
      src={icon()}
      alt=""
      style="display: block; width: 20%; margin-left: 5%; border-radius: 100px;"
    />
    <img
      src={icon()}
      alt=""
      style="display: block; width: 15%; margin-left: 75%; border-radius: 100px;"
    />
  </ParallaxLayer>

  <ParallaxLayer
    offset="2"
    rate="-0.3"
    style="display: flex; align-items: center; justify-content: center;"
  />

  <ParallaxLayer
    offset="0"
    rate="0.1"
    style="display: flex; align-items: center; justify-content: center;"
  >
    <!--    <h2-->
    <!--      class="hero glitch layers"-->
    <!--      data-text="tubone24"-->
    <!--      on:click={() => parallax.scrollTo(3, { selector: ".clients-main" })}-->
    <!--      on:keyup={(e) =>-->
    <!--        e.key === "Enter" &&-->
    <!--        parallax.scrollTo(3, { selector: ".clients-main" })}-->
    <!--    >-->
    <!--      <span>tubone24</span>-->
    <!--    </h2>-->
    <h1 contenteditable spellcheck="false">tubone24</h1>
  </ParallaxLayer>

  <ParallaxLayer
    offset="1"
    rate="0.1"
    style="display: flex; align-items: center; justify-content: center;"
  >
    <img
      src={icon()}
      alt=""
      class="my-icon"
      style="width: 20%; border-radius: 100px;"
      on:click={() => parallax.scrollTo(3, { selector: ".clients-main" })}
      on:keyup={(e) =>
        e.key === "Enter" &&
        parallax.scrollTo(3, { selector: ".clients-main" })}
      tabindex="0"
    />
    <h2 class="aboutme">Web Developer</h2>
  </ParallaxLayer>

  <ParallaxLayer
    offset="2"
    rate="-0"
    style="display: flex; align-items: center; justify-content: center;"
  >
    <h2 spellcheck="false" class="rainbow-text">Thankyou</h2>
  </ParallaxLayer>
</Parallax>

<style>
  @import url("https://fonts.googleapis.com/css?family=Exo:800&display=swap");
  @import url("https://fonts.googleapis.com/css?family=Exo+2:200i");
  @import url("https://fonts.googleapis.com/css2?family=Lora:ital@1&display=swap");
  :global(body) {
    padding: 0;
  }

  :root {
    /* Set neon color */
    --neon-text-color: #f40;
    --neon-border-color: #08f;
  }

  h1 {
    font-size: 6rem;
    font-weight: 200;
    font-style: italic;
    font-family: "Exo 2", sans-serif;
    color: #fff;
    padding: 4rem 6rem 5.5rem;
    border: 0.4rem solid #fff;
    border-radius: 2rem;
    text-transform: uppercase;
    animation: flicker 1.5s infinite alternate;
  }

  h1::-moz-selection {
    background-color: var(--neon-border-color);
    color: var(--neon-text-color);
  }

  h1::selection {
    background-color: var(--neon-border-color);
    color: var(--neon-text-color);
  }

  h1:focus {
    outline: none;
  }

  /* Animate neon flicker */
  @keyframes flicker {
    0%,
    19%,
    21%,
    23%,
    25%,
    54%,
    56%,
    100% {
      text-shadow: -0.2rem -0.2rem 1rem #fff, 0.2rem 0.2rem 1rem #fff,
        0 0 2rem var(--neon-text-color), 0 0 4rem var(--neon-text-color),
        0 0 6rem var(--neon-text-color), 0 0 8rem var(--neon-text-color),
        0 0 10rem var(--neon-text-color);

      box-shadow: 0 0 0.5rem #fff, inset 0 0 0.5rem #fff,
        0 0 2rem var(--neon-border-color),
        inset 0 0 2rem var(--neon-border-color),
        0 0 4rem var(--neon-border-color),
        inset 0 0 4rem var(--neon-border-color);
    }

    20%,
    24%,
    55% {
      text-shadow: none;
      box-shadow: none;
    }
  }

  .my-icon {
    cursor: pointer;
  }
  img:focus {
    outline: 1px dotted gray;
  }
  img:focus:not(:focus-visible) {
    outline: none;
  }
  .my-icon:focus-visible {
    outline: 2px dotted purple;
  }

  h2 {
    margin: 0;
  }
  .aboutme {
    position: absolute;
    font-family: "Lora", cursive;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 12vmin;
    text-transform: uppercase;
    letter-spacing: 0.075em;
    color: #020202;
    -webkit-text-stroke: 0.02em #fff;
    text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
      -0.066em 0 0 rgba(140, 168, 141, 0.9);
    animation: glitch-shadow 8s infinite linear,
      glitch-flicker 7s infinite linear;
  }

  .rainbow-text {
    position: absolute;
    font-family: "Lora", cursive;
    top: 50%;
    left: 50%;
    font-size: 12vmin;
    background: #ca4246;
    background-color: #ca4246;
    background: conic-gradient(
      #ca4246 16.666%,
      #e16541 16.666%,
      #e16541 33.333%,
      #f18f43 33.333%,
      #f18f43 50%,
      #8b9862 50%,
      #8b9862 66.666%,
      #476098 66.666%,
      #476098 83.333%,
      #a7489b 83.333%
    );

    /* Set thee background size and repeat properties. */
    background-size: 57%;
    background-repeat: repeat;

    /* Use the text as a mask for the background. */
    /* This will show the gradient as a text color rather than element bg. */
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;

    /* Animate the text when loading the element. */
    /* This animates it on page load and when hovering out. */
    animation: rainbow-text-animation-rev 0.5s ease forwards;

    cursor: pointer;
  }

  /* Add animation on hover. */
  .rainbow-text:hover {
    animation: rainbow-text-animation 0.5s ease forwards;
  }

  /* Move the background and make it larger. */
  /* Animation shown when hovering over the text. */
  @keyframes rainbow-text-animation {
    0% {
      background-size: 57%;
      background-position: 0 0;
    }
    20% {
      background-size: 57%;
      background-position: 0 1em;
    }
    100% {
      background-size: 300%;
      background-position: -9em 1em;
    }
  }

  /* Move the background and make it smaller. */
  /* Animation shown when entering the page and after the hover animation. */
  @keyframes rainbow-text-animation-rev {
    0% {
      background-size: 300%;
      background-position: -9em 1em;
    }
    20% {
      background-size: 57%;
      background-position: 0 1em;
    }
    100% {
      background-size: 57%;
      background-position: 0 0;
    }
  }

  @keyframes glitch-flicker {
    0% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }

    10% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }
    10.1% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    10.6% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    10.7% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }

    11% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }
    11.1% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    11.6% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    11.7% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }

    50% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }
    50.1% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    51.6% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    51.7% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }

    70% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }
    70.1% {
      color: #000;
      -webkit-text-stroke-color: transparent;
    }
    70.6% {
      color: #000;
      -webkit-text-stroke-color: transparent;
    }
    70.7% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }

    73% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }
    73.1% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    73.6% {
      color: transparent;
      -webkit-text-stroke-color: transparent;
    }
    73.7% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }

    100% {
      color: #000;
      -webkit-text-stroke-color: #fff;
    }
  }

  @keyframes glitch-shadow {
    0% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    3% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    3.1% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    3.6% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    3.7% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    6% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    6.1% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    6.6% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    6.7% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    16% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    16.1% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9), 0 0 0 rgba(140, 168, 141, 0.9);
    }
    16.6% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9), 0 0 0 rgba(140, 168, 141, 0.9);
    }
    16.7% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    50% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    50.1% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        0 0 0 rgba(140, 168, 141, 0.9);
    }
    50.6% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        0 0 0 rgba(140, 168, 141, 0.9);
    }
    50.7% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    62% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    62.1% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    62.6% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    62.7% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    63% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
    63.1% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9), 0 0 0 rgba(140, 168, 141, 0.9);
    }
    63.6% {
      text-shadow: 0 0 0 rgba(130, 44, 44, 0.9), 0 0 0 rgba(140, 168, 141, 0.9);
    }
    63.7% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }

    100% {
      text-shadow: 0.066em 0 0 rgba(130, 44, 44, 0.9),
        -0.066em 0 0 rgba(140, 168, 141, 0.9);
    }
  }
  .hero {
    font-size: clamp(40px, 10vw, 100px);
    line-height: 1;
    display: inline-block;
    color: #98d598;
    z-index: 2;
    letter-spacing: 10px;

    /* Bright things in dark environments usually cast that light, giving off a glow */
    filter: drop-shadow(0 1px 3px);
  }

  .layers {
    position: relative;
  }

  .layers::before,
  .layers::after {
    content: attr(data-text);
    position: absolute;
    width: 110%;
    z-index: -1;
  }

  .layers::before {
    top: 10px;
    left: 15px;
    color: #e0287d;
  }

  .layers::after {
    top: 5px;
    left: -10px;
    color: #1bc7fb;
  }

  .single-path {
    clip-path: polygon(
      0% 12%,
      53% 12%,
      53% 26%,
      25% 26%,
      25% 86%,
      31% 86%,
      31% 0%,
      53% 0%,
      53% 84%,
      92% 84%,
      92% 82%,
      70% 82%,
      70% 29%,
      78% 29%,
      78% 65%,
      69% 65%,
      69% 66%,
      77% 66%,
      77% 45%,
      85% 45%,
      85% 26%,
      97% 26%,
      97% 28%,
      84% 28%,
      84% 34%,
      54% 34%,
      54% 89%,
      30% 89%,
      30% 58%,
      83% 58%,
      83% 5%,
      68% 5%,
      68% 36%,
      62% 36%,
      62% 1%,
      12% 1%,
      12% 34%,
      60% 34%,
      60% 57%,
      98% 57%,
      98% 83%,
      1% 83%,
      1% 53%,
      91% 53%,
      91% 84%,
      8% 84%,
      8% 83%,
      4% 83%
    );
  }

  .paths {
    animation: paths 5s step-end infinite;
  }

  @keyframes paths {
    0% {
      clip-path: polygon(
        0% 43%,
        83% 43%,
        83% 22%,
        23% 22%,
        23% 24%,
        91% 24%,
        91% 26%,
        18% 26%,
        18% 83%,
        29% 83%,
        29% 17%,
        41% 17%,
        41% 39%,
        18% 39%,
        18% 82%,
        54% 82%,
        54% 88%,
        19% 88%,
        19% 4%,
        39% 4%,
        39% 14%,
        76% 14%,
        76% 52%,
        23% 52%,
        23% 35%,
        19% 35%,
        19% 8%,
        36% 8%,
        36% 31%,
        73% 31%,
        73% 16%,
        1% 16%,
        1% 56%,
        50% 56%,
        50% 8%
      );
    }

    5% {
      clip-path: polygon(
        0% 29%,
        44% 29%,
        44% 83%,
        94% 83%,
        94% 56%,
        11% 56%,
        11% 64%,
        94% 64%,
        94% 70%,
        88% 70%,
        88% 32%,
        18% 32%,
        18% 96%,
        10% 96%,
        10% 62%,
        9% 62%,
        9% 84%,
        68% 84%,
        68% 50%,
        52% 50%,
        52% 55%,
        35% 55%,
        35% 87%,
        25% 87%,
        25% 39%,
        15% 39%,
        15% 88%,
        52% 88%
      );
    }

    30% {
      clip-path: polygon(
        0% 53%,
        93% 53%,
        93% 62%,
        68% 62%,
        68% 37%,
        97% 37%,
        97% 89%,
        13% 89%,
        13% 45%,
        51% 45%,
        51% 88%,
        17% 88%,
        17% 54%,
        81% 54%,
        81% 75%,
        79% 75%,
        79% 76%,
        38% 76%,
        38% 28%,
        61% 28%,
        61% 12%,
        55% 12%,
        55% 62%,
        68% 62%,
        68% 51%,
        0% 51%,
        0% 92%,
        63% 92%,
        63% 4%,
        65% 4%
      );
    }

    45% {
      clip-path: polygon(
        0% 33%,
        2% 33%,
        2% 69%,
        58% 69%,
        58% 94%,
        55% 94%,
        55% 25%,
        33% 25%,
        33% 85%,
        16% 85%,
        16% 19%,
        5% 19%,
        5% 20%,
        79% 20%,
        79% 96%,
        93% 96%,
        93% 50%,
        5% 50%,
        5% 74%,
        55% 74%,
        55% 57%,
        96% 57%,
        96% 59%,
        87% 59%,
        87% 65%,
        82% 65%,
        82% 39%,
        63% 39%,
        63% 92%,
        4% 92%,
        4% 36%,
        24% 36%,
        24% 70%,
        1% 70%,
        1% 43%,
        15% 43%,
        15% 28%,
        23% 28%,
        23% 71%,
        90% 71%,
        90% 86%,
        97% 86%,
        97% 1%,
        60% 1%,
        60% 67%,
        71% 67%,
        71% 91%,
        17% 91%,
        17% 14%,
        39% 14%,
        39% 30%,
        58% 30%,
        58% 11%,
        52% 11%,
        52% 83%,
        68% 83%
      );
    }

    76% {
      clip-path: polygon(
        0% 26%,
        15% 26%,
        15% 73%,
        72% 73%,
        72% 70%,
        77% 70%,
        77% 75%,
        8% 75%,
        8% 42%,
        4% 42%,
        4% 61%,
        17% 61%,
        17% 12%,
        26% 12%,
        26% 63%,
        73% 63%,
        73% 43%,
        90% 43%,
        90% 67%,
        50% 67%,
        50% 41%,
        42% 41%,
        42% 46%,
        50% 46%,
        50% 84%,
        96% 84%,
        96% 78%,
        49% 78%,
        49% 25%,
        63% 25%,
        63% 14%
      );
    }

    90% {
      clip-path: polygon(
        0% 41%,
        13% 41%,
        13% 6%,
        87% 6%,
        87% 93%,
        10% 93%,
        10% 13%,
        89% 13%,
        89% 6%,
        3% 6%,
        3% 8%,
        16% 8%,
        16% 79%,
        0% 79%,
        0% 99%,
        92% 99%,
        92% 90%,
        5% 90%,
        5% 60%,
        0% 60%,
        0% 48%,
        89% 48%,
        89% 13%,
        80% 13%,
        80% 43%,
        95% 43%,
        95% 19%,
        80% 19%,
        80% 85%,
        38% 85%,
        38% 62%
      );
    }

    1%,
    7%,
    33%,
    47%,
    78%,
    93% {
      clip-path: none;
    }
  }

  .movement {
    position: relative;
    animation: movement 8s step-end infinite;
  }

  @keyframes movement {
    0% {
      top: 0px;
      left: -20px;
    }

    15% {
      top: 10px;
      left: 10px;
    }

    60% {
      top: 5px;
      left: -10px;
    }

    75% {
      top: -5px;
      left: 20px;
    }

    100% {
      top: 10px;
      left: 5px;
    }
  }

  .opacity {
    animation: opacity 5s step-end infinite;
  }

  @keyframes opacity {
    0% {
      opacity: 0.1;
    }

    5% {
      opacity: 0.7;
    }

    30% {
      opacity: 0.4;
    }

    45% {
      opacity: 0.6;
    }

    76% {
      opacity: 0.4;
    }

    90% {
      opacity: 0.8;
    }

    1%,
    7%,
    33%,
    47%,
    78%,
    93% {
      opacity: 0;
    }
  }

  .font {
    animation: font 7s step-end infinite;
  }

  @keyframes font {
    0% {
      font-weight: 100;
      color: #e0287d;
      filter: blur(3px);
    }

    20% {
      font-weight: 500;
      color: #98d598;
      filter: blur(0);
    }

    50% {
      font-weight: 300;
      color: #1bc7fb;
      filter: blur(2px);
    }

    60% {
      font-weight: 700;
      color: #98d598;
      filter: blur(0);
    }

    90% {
      font-weight: 500;
      color: #e0287d;
      filter: blur(6px);
    }
  }

  .glitch span {
    animation: paths 5s step-end infinite;
    font-family: "Exo";
  }

  .glitch::before {
    animation: paths 5s step-end infinite, opacity 5s step-end infinite,
      font 8s step-end infinite, movement 10s step-end infinite;
  }

  .glitch::after {
    animation: paths 5s step-end infinite, opacity 5s step-end infinite,
      font 7s step-end infinite, movement 8s step-end infinite;
  }
</style>
