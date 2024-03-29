<script type="ts">
  import "../styles/globals.css";
  import SectionTitle from "../lib/SectionTitle.svelte";
  import LinkToSection from "../lib/LinkToSection.svelte";
  import {onMount} from "svelte";
  import Particles from "../lib/Particles.svelte";
  import ProjectsList from "../lib/ProjectsList.svelte";
  import CardGrid from "../lib/CardGrid/CardGrid.svelte";
  import Card from "../lib/CardGrid/Card.svelte";
  import Achievements from "../lib/achievements/Achievements.svelte";

  let isMobile: boolean | null = null;
  onMount(() => {
    isMobile = window.innerWidth <= 768;
  });
</script>

<svelte:head>
  <title>Nathan Wang (thecodingwizard)</title>
</svelte:head>

<div class="bg-blueGray-900">
  <div class="min-h-screen flex flex-col justify-center relative">
    {#if isMobile !== null}
      <Particles isMobile={isMobile} />
    {/if}

    <div class="container z-10">
      <SectionTitle accentText="Hi there! I'm" title="Nathan Wang" />
      <div class="h-4 sm:h-0"></div>
      <div class="text-body-container">
        <LinkToSection title="About Me" href="about">
          I love programming, especially competitive programming and web development.
          I also play a lot of board games and social deduction games like Secret Hitler!
        </LinkToSection>
        <LinkToSection title="Projects" href="projects">
          I run the USACO Guide and the Competitive Programming Initiative.
        </LinkToSection>
        <LinkToSection title="Achievements" href="achievements">
          I'm a 3x USACO Finalist and a 5x AIME Qualifier.
        </LinkToSection>
        <LinkToSection title="Work Experience" href="experience">
          I enjoy teaching competitive programming!
        </LinkToSection>
        <LinkToSection title="School" href="school">
          I'm currently a student at Monta Vista High School, where I'm part of Model United Nations and Future Business Leaders of America.
        </LinkToSection>
      </div>
      <div class="h-6 md:h-8 xl:h-16"></div>
      <div class="font-mono text-blueGray-400 sm:text-lg md:text-xl">
        <a class="link" href="mailto:nathan.r.wang@gmail.com" target="_blank">Email</a> · <a class="link" href="https://github.com/thecodingwizard" target="_blank">Github</a> · <a class="link" href="https://www.linkedin.com/in/nathan-r-wang/" target="_blank">Linkedin</a>
      </div>
    </div>
  </div>

  <div class="container" id="about">
    <SectionTitle accentText="01" title="About Me" />
    <div class="text-body-container">
      <p>
        Ever since I embarked on my programming journey as a young child, I've been entranced by the power and flexibility of code.
      </p>
      <p>
        Today, I'm an avid competitive programmer and web developer. Programming is my superpower: With it, what I can create is limited only by my imagination!
      </p>
      <p>
        Outside of programming, I play a lot of board games, especially social deduction games (my personal favorite is Secret Hitler). I also enjoy discussing politics and government!
      </p>
      <p>
        I strive to bring energy, technical knowledge, and a strong desire to learn with me wherever I go.
      </p>
    </div>
  </div>

  <div class="container" id="projects">
    <SectionTitle accentText="02" title="Projects" />
    <div class="text-body-container">
      <p>
        I'm always working on something new. Below are a few of my favorite projects!
      </p>
    </div>
    <div class="h-8 lg:h-12"></div>
    <ProjectsList />
  </div>

  <div class="container" id="achievements">
    <SectionTitle accentText="03" title="Achievements" />
    <Achievements />
  </div>

  <div class="container" id="experience">
    <SectionTitle accentText="04" title="Work Experience" />
    <div class="text-body-container">
      <p>
        I've taught USACO Gold Advanced at Alphastar Academy in summer 2020 and 2021. I also do private USACO tutoring from time to time.
      </p>
    </div>
  </div>

  <div class="container" id="school">
    <SectionTitle accentText="05" title="School" />
    <div class="text-body-container">
      <p>
        I'm currently a student at Monta Vista High School, where I'm part of some amazing clubs!
      </p>
    </div>
    <div class="h-8 lg:h-12"></div>
    <CardGrid>
      <Card title="Model UN" link="https://montavistamun.com/">
        In Model United Nations, members learn about teamwork, negotiation, and diplomacy as we simulate the real United Nations!
      </Card>
      <Card title="FBLA" link="http://mvfbla.com/">
        In Future Business Leaders of America, I learn more about how to run a business and become a successful entrepreneur!
      </Card>
      <Card title="AI Club" link="https://mvaiclub.github.io/">
        Monta Vista AI Club teaches its members about artificial intelligence topics including machine learning, deep learning, and various applications of AI.
      </Card>
      <Card title="Competitive Programming Club" link="https://mvcpc.org/">
        Monta Vista Competitive Programming Club prepares members for competitive programming competitions like the USA Computing Olympiad.
      </Card>
    </CardGrid>
  </div>

  <div class="container" id="contact">
    <SectionTitle accentText="06" title="Contact Me" />
    <div class="font-mono text-blueGray-400 sm:text-lg md:text-xl">
      <a class="link" href="mailto:nathan.r.wang@gmail.com" target="_blank">Email</a> · <a class="link" href="https://github.com/thecodingwizard" target="_blank">Github</a> · <a class="link" href="https://www.linkedin.com/in/nathan-r-wang/" target="_blank">Linkedin</a>
    </div>
  </div>

  <div class="h-8 md:h-12 lg:h-16"></div>

  <div class="container pb-6 md:pb-12 lg:pb-24">
    <div class="font-mono text-blueGray-400 text-xs md:text-sm lg:text-base">
      Copyright 2021 Nathan Wang.<br />
      This site is built with <a class="link" href="https://svelte.dev/" target="_blank">Svelte</a> and <a class="link" href="https://tailwindcss.com/" target="_blank">Tailwind CSS</a>.
      View the source code on <a class="link" href="https://github.com/thecodingwizard/personal-website" target="_blank">Github</a>.
    </div>
  </div>
</div>