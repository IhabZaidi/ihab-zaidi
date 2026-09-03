<script setup>
import { ref } from 'vue'

const mobileOpen = ref(false)
const toggleMenu = () => mobileOpen.value = !mobileOpen.value

const techStack = [
  { name: 'Flutter', cat: 'Mobile', color: 'bg-sky-50 text-sky-700 border-sky-200' },
  { name: 'Vue.js', cat: 'Frontend', color: 'bg-emerald-50 text-emerald-700 border-emerald-200' },
  { name: 'React.js', cat: 'Frontend', color: 'bg-cyan-50 text-cyan-700 border-cyan-200' },
  { name: 'Next.js', cat: 'Frontend', color: 'bg-zinc-50 text-zinc-700 border-zinc-200' },
  { name: 'Odoo', cat: 'ERP', color: 'bg-purple-50 text-purple-700 border-purple-200' },
  { name: 'OWL', cat: 'Odoo Frontend', color: 'bg-violet-50 text-violet-700 border-violet-200' },
  { name: 'Express.js', cat: 'Backend', color: 'bg-neutral-50 text-neutral-700 border-neutral-200' },
  { name: 'Docker', cat: 'DevOps', color: 'bg-blue-50 text-blue-700 border-blue-200' },
  { name: 'Cyber Security', cat: 'Security', color: 'bg-red-50 text-red-700 border-red-200' },
  { name: 'Reverse Eng.', cat: 'Security', color: 'bg-amber-50 text-amber-700 border-amber-200' },
  { name: 'n8n', cat: 'Automation', color: 'bg-pink-50 text-pink-700 border-pink-200' },
  { name: 'Automation', cat: 'Workflow', color: 'bg-teal-50 text-teal-700 border-teal-200' },
  { name: 'AI', cat: 'AI • Daily', color: 'bg-fuchsia-50 text-fuchsia-700 border-fuchsia-200' },
]

const projects = [
  {
    title: 'Langaroo',
    url: 'https://langaroo.co/',
    desc: 'Landing page for Langaroo mobile app — translated chat, audio & video calls, text and image translation and more. Real-time cross-language communication.',
    tags: ['Landing Page', 'Mobile App', 'Chat • Calls • Images'],
    live: 'https://langaroo.co/',
    accent: 'from-violet-500 to-indigo-500',
    type: 'Landing Page • Mobile App'
  },
  {
    title: 'Invento',
    url: 'https://invento-kappa.vercel.app/',
    desc: 'Landing page for Invento mobile app — POS inventory tracker. Showcases features, store management & drives downloads.',
    tags: ['Landing Page', 'Mobile App', 'React'],
    live: 'https://invento-kappa.vercel.app/',
    accent: 'from-emerald-500 to-teal-500',
    type: 'Landing Page • Mobile App'
  },
  {
    title: 'Subtitles.tech',
    url: 'https://subtitles.tech/',
    desc: 'Full web app — transcribe & translate any video/audio in seconds, add dubbing to any video, get summary and more. Fast, AI-powered for creators.',
    tags: ['Web App', 'Transcribe • Translate', 'Dubbing • Summary'],
    live: 'https://subtitles.tech/',
    accent: 'from-sky-500 to-cyan-500',
    type: 'Web App'
  },
  {
    title: 'Arabyati',
    url: 'https://arabyati.com/ar/%D8%A7%D9%84%D8%B1%D8%A6%D9%8A%D8%B3%D9%8A%D8%A9/',
    desc: 'Landing page for Arabyati app — teaches non-Arab speakers Arabic in a fun, interactive way. Short lessons, drama videos & smart exercises from beginner to fluent.',
    tags: ['Landing Page', 'Education', 'Arabic LMS'],
    live: 'https://arabyati.com/ar/%D8%A7%D9%84%D8%B1%D8%A6%D9%8A%D8%B3%D9%8A%D8%A9/',
    accent: 'from-amber-500 to-orange-500',
    type: 'Landing Page • Education'
  },
  {
    title: 'MarketFy Pro',
    url: 'https://www.marketfy.pro/',
    desc: 'Chrome extension + web app — helps sellers mass-post products on Facebook Marketplace across all 58 Algerian wilayas in a few clicks. Save hours of manual work.',
    tags: ['Chrome Extension', 'Web App', 'Automation'],
    live: 'https://www.marketfy.pro/',
    accent: 'from-emerald-500 to-teal-500',
    type: 'Extension • Web App'
  },
  {
    title: 'Ecozed — Ad Content Studio',
    url: 'https://ecozed-ld-promt-gen.vercel.app/',
    desc: 'Open-source AI tool for marketers — create full ad content in minutes: script, text, image, video & landing page from one AI prompt. Free, fast, minutes not hours.',
    tags: ['Open Source', 'AI Tool', 'Ads • Landing Page'],
    live: 'https://ecozed-ld-promt-gen.vercel.app/',
    accent: 'from-fuchsia-500 to-purple-500',
    type: 'Open Source • AI'
  },
  {
    title: 'Delivoc',
    url: 'https://www.delivoc.com/',
    desc: 'Landing page for Delivoc app — turn travel into income. Connects travelers with delivery requests along their route, flexible shipping options & secure mediated payments.',
    tags: ['Landing Page', 'Marketplace', 'Logistics'],
    live: 'https://www.delivoc.com/',
    accent: 'from-orange-500 to-red-500',
    type: 'Landing Page • Mobile App'
  },
  {
    title: 'Almas Online',
    url: 'https://almas-online.com/',
    desc: 'E-commerce store for selling diamonds in Dubai — recreation with new framework, fixing performance issues. Fast, luxury UX optimized for jewelry sales.',
    tags: ['E-commerce', 'Rebuild', 'Performance Fix'],
    live: 'https://almas-online.com/',
    accent: 'from-zinc-700 to-zinc-900',
    type: 'E-commerce • Rebuild'
  },
  {
    title: 'MagicTouch Plus',
    url: 'https://magictouchplus.com/',
    desc: 'PPF products showcase site — fixed bugs and added new features. 30 years PPF expertise, OEM solutions, Magic Shield/Core product galleries.',
    tags: ['Bug Fix', 'Features', 'E-commerce Showcase'],
    live: 'https://magictouchplus.com/',
    accent: 'from-slate-600 to-slate-800',
    type: 'Maintenance • Features'
  }
]

const iosApps = [
  {
    name: 'Translation: voice and text',
    subtitle: 'Speak & Translate instantly',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple211/v4/a3/b2/34/a3b234ba-26d0-c8da-0cea-59842fa485dd/AppIcon-0-0-1x_U007emarketing-0-10-0-85-220.png/512x512bb.jpg',
    desc: 'Voice translator with speech-to-text, real-time translation in 40+ languages, text-to-speech & offline mode.',
    category: 'Productivity',
    url: 'https://apps.apple.com/us/app/translation-voice-and-text/id6740727522'
  },
  {
    name: 'Fitvento: Workout Tracker',
    subtitle: 'Offline Timer, Tracker & Voice',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple211/v4/c3/19/68/c3196815-9323-5f53-3496-fad9bbca4f74/AppIcon-0-0-1x_U007emarketing-0-10-0-0-85-220.png/512x512bb.jpg',
    desc: 'Custom workout routines, real-time voice feedback and progress tracking — hands-free fitness companion.',
    category: 'Health & Fitness',
    url: 'https://apps.apple.com/us/app/fitvento-workout-tracker/id6742684642'
  },
  {
    name: 'HIIT Interval Timer & Tracker',
    subtitle: 'Offline Fitness Routines',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple221/v4/8d/64/0d/8d640dd0-f4fe-f106-31da-a5cf4df47189/AppIcon-0-0-1x_U007emarketing-0-10-0-0-85-220.png/512x512bb.jpg',
    desc: 'Build HIIT, Tabata & CrossFit timers with voice cues, tracking, reminders and 20+ languages.',
    category: 'Health & Fitness',
    url: 'https://apps.apple.com/us/app/hiit-interval-timer-tracker/id6742692409'
  },
  {
    name: 'WhiteSync: Whiteboard Drawing',
    subtitle: 'Collaborate, Sketch and Sync',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple221/v4/f6/c8/90/f6c89094-d00e-e1ee-1904-e7f3ddb2bc11/AppIcon-0-0-1x_U007emarketing-0-10-0-0-85-220.png/512x512bb.jpg',
    desc: 'Real-time collaborative whiteboard — draw together over WiFi or cloud, sync sketches instantly.',
    category: 'Productivity',
    url: 'https://apps.apple.com/us/app/whitesync-whiteboard-drawing/id6742335781'
  },
  {
    name: 'Timy: Calculator & Converter',
    subtitle: 'Time Calculator',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple221/v4/31/fb/43/31fb43c5-2949-7352-a9d9-1de3c02cc9c1/AppIcon-0-0-1x_U007emarketing-0-10-0-0-85-220.png/512x512bb.jpg',
    desc: 'Master time: calculate, convert, find age & durations. 24 languages, history & PDF export.',
    category: 'Productivity',
    url: 'https://apps.apple.com/us/app/timy-calculator-converter/id6744637330'
  },
  {
    name: 'FlipRate: Money Converter',
    subtitle: 'Currency Calculator',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple221/v4/b3/54/6f/b3546f73-3e00-15ca-35a0-6846d9c4d0ba/AppIcon-0-0-1x_U007emarketing-0-10-0-0-85-220.png/512x512bb.jpg',
    desc: 'Fast money converter for 160+ currencies, 5 free/day, history tracking & exchange rates in 24 languages.',
    category: 'Finance',
    url: 'https://apps.apple.com/us/app/fliprate-simple-money-convert/id6744040825'
  },
  {
    name: 'ShadeFinder: Color Identifier',
    subtitle: 'Color Wheel & Palette',
    icon: 'https://is1-ssl.mzstatic.com/image/thumb/Purple221/v4/59/be/18/59be18d6-786d-1ddf-907f-305ad947eaaf/AppIcon-0-0-1x_U007emarketing-0-10-0-0-85-220.png/512x512bb.jpg',
    desc: 'Snap any color with camera — get HEX, RGB & name, generate palettes with color wheel & export.',
    category: 'Utilities',
    url: 'https://apps.apple.com/us/app/shadefinder-color-identifier/id6743338684'
  }
]

const androidApps = [
  {
    name: 'Lecture Translation',
    subtitle: '143 languages • Real-time speeches',
    icon: 'https://play-lh.googleusercontent.com/RJpAsQsuduYyckuOdQZyHeg4hdsbzMp1gA_wmUXkiI33jLpI0FSjdcQLmLjERYH1FDhZf14VaRu8D2HlNewb=w512-h512-rw',
    desc: 'Translate live speeches & lectures into 143 languages in real time — host streams, listeners follow via text/audio, plus TV display for khutbahs.',
    category: 'Tools',
    url: 'https://play.google.com/store/apps/details?id=com.itsourceone.lecture.translation&hl=en'
  },
  {
    name: 'IPEDIA IQ',
    subtitle: '120+ languages • Personalization',
    icon: 'https://play-lh.googleusercontent.com/CWZmMzZs_THrAzHR94-lRcYULGfL5zuULoTNuAIRWv6PipTZVaFZ-hMZ5odc0-iAXAXYSV1V7VYE0o-LgGPR=w512-h512-rw',
    desc: 'Two-way speech & text translation in 120+ languages, photo/scan translation — the ultimate communication solution.',
    category: 'Communication',
    url: 'https://play.google.com/store/apps/details?id=com.Ipedia.IQ&hl=en'
  },
  {
    name: 'Khutbah Translation',
    subtitle: '143 languages • Mosque TV mode',
    icon: 'https://play-lh.googleusercontent.com/MGM4x0lqfK9HB7n1ByLT_wfOQZ9zpgze308M0jM_AtswSOU8qac6ye7N67AqAP1Iy0m4PYMk74BWRfMk0yV6SGs=w512-h512-rw',
    desc: 'Same real-time engine as Lecture — translate khutbahs live to 143 languages, display on TVs, listeners use text/audio with no subscription needed.',
    category: 'Tools',
    url: 'https://play.google.com/store/apps/details?id=com.itsourceone.khutbah.translation&hl=en'
  }
]

const scrollTo = (id) => {
  mobileOpen.value = false
  document.querySelector(id)?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <!-- NAV -->
  <header class="sticky top-0 z-50 bg-white/80 backdrop-blur-md border-b border-zinc-100">
    <nav class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
      <a href="#" class="flex items-center gap-3">
        <div class="w-9 h-9 rounded-xl bg-zinc-900 text-white flex items-center justify-center font-bold text-sm tracking-widest">IZ</div>
        <span class="font-semibold tracking-tight text-zinc-900">Ihab ZAIDI</span>
        <span class="hidden sm:inline text-xs px-2 py-1 rounded-full bg-zinc-100 text-zinc-600 border border-zinc-200">Senior Dev</span>
      </a>

      <!-- desktop -->
      <div class="hidden md:flex items-center gap-8">
        <a @click.prevent="scrollTo('#projects')" href="#projects" class="text-sm text-zinc-600 hover:text-zinc-900 transition">Projects</a>
        <a @click.prevent="scrollTo('#apps')" href="#apps" class="text-sm text-zinc-600 hover:text-zinc-900 transition">iOS</a>
        <a @click.prevent="scrollTo('#android')" href="#android" class="text-sm text-zinc-600 hover:text-zinc-900 transition">Android</a>
        <a @click.prevent="scrollTo('#stack')" href="#stack" class="text-sm text-zinc-600 hover:text-zinc-900 transition">Stack</a>
        <a @click.prevent="scrollTo('#experience')" href="#experience" class="text-sm text-zinc-600 hover:text-zinc-900 transition">Experience</a>
        <a @click.prevent="scrollTo('#contact')" href="#contact" class="ml-2 inline-flex items-center gap-2 bg-zinc-900 text-white px-5 py-2.5 rounded-full text-sm font-medium hover:bg-black transition">
          Contact me
          <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M13 5l7 7-7 7"/></svg>
        </a>
      </div>

      <!-- mobile btn -->
      <button @click="toggleMenu" class="md:hidden p-2 rounded-lg border border-zinc-200">
        <svg v-if="!mobileOpen" class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M4 6h16M4 12h16M4 18h16"/></svg>
        <svg v-else class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M6 18L18 6M6 6l12 12"/></svg>
      </button>
    </nav>

    <!-- mobile menu -->
    <div v-if="mobileOpen" class="md:hidden border-t border-zinc-100 bg-white px-4 py-4 space-y-3">
      <a @click.prevent="scrollTo('#projects')" href="#projects" class="block py-2 text-sm text-zinc-700">Projects</a>
      <a @click.prevent="scrollTo('#apps')" href="#apps" class="block py-2 text-sm text-zinc-700">iOS Apps (7)</a>
      <a @click.prevent="scrollTo('#android')" href="#android" class="block py-2 text-sm text-zinc-700">Android (3)</a>
      <a @click.prevent="scrollTo('#stack')" href="#stack" class="block py-2 text-sm text-zinc-700">Stack</a>
      <a @click.prevent="scrollTo('#experience')" href="#experience" class="block py-2 text-sm text-zinc-700">Experience</a>
      <a @click.prevent="scrollTo('#contact')" href="#contact" class="block mt-2 text-center bg-zinc-900 text-white py-3 rounded-full text-sm font-medium">Contact me</a>
    </div>
  </header>

  <!-- HERO -->
  <section class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 pt-10 pb-8 sm:pt-16 sm:pb-12">
    <div class="grid lg:grid-cols-12 gap-8 items-center">
      <div class="lg:col-span-7">
        <div class="inline-flex items-center gap-2 text-xs font-medium px-3 py-1.5 rounded-full bg-violet-50 border border-violet-200 text-violet-700 mb-5">
          <span class="w-2 h-2 rounded-full bg-violet-600 animate-pulse"></span>
          Available for new opportunities
        </div>
        <h1 class="text-4xl sm:text-5xl lg:text-[56px] font-semibold tracking-tight text-zinc-900 leading-[0.95]">
          Ihab <span class="font-light text-zinc-400">ZAIDI</span>
        </h1>
        <p class="mt-3 text-lg sm:text-xl text-zinc-600 font-medium">Senior Software Developer & Team Lead</p>
        <p class="mt-4 text-[15px] leading-7 text-zinc-500 max-w-xl">
          <span class="font-medium text-zinc-700">13 years</span> in dev — first production app in <span class="font-medium text-zinc-700">2015 (.NET VB)</span>, now
          <span class="font-medium text-zinc-700">5+ years as Senior & Team Lead at ItsourceOne</span>.
          Based in <span class="font-medium text-zinc-700">Algeria</span> — I craft clean web & mobile experiences with Vue, React, Flutter & Odoo, use <span class="font-medium text-zinc-700">AI daily</span> as a coding assistant, and stream to teach others how to get started in the digital world.
        </p>

        <div class="mt-7 flex flex-wrap gap-3">
          <a @click.prevent="scrollTo('#projects')" href="#projects" class="inline-flex items-center gap-2 bg-zinc-900 text-white px-6 py-3 rounded-full text-sm font-medium hover:bg-black transition">
            View Projects
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M13 5l7 7-7 7"/></svg>
          </a>
          <a href="mailto:ihabeddinezaidi@gmail.com" class="inline-flex items-center gap-2 bg-white border border-zinc-200 px-6 py-3 rounded-full text-sm font-medium text-zinc-700 hover:border-zinc-300 hover:bg-zinc-50 transition">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="1.7" viewBox="0 0 24 24"><path d="M4 4h16v16H4z"/><path d="M4 7l8 6 8-6"/></svg>
            ihabeddinezaidi@gmail.com
          </a>
          <a href="https://wa.me/213797332534" target="_blank" class="inline-flex items-center gap-2 bg-emerald-500 text-white px-6 py-3 rounded-full text-sm font-medium hover:bg-emerald-600 transition">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M19.05 4.91A9.82 9.82 0 0012.04 2a9.86 9.86 0 00-8.5 14.86L2 22l5.26-1.38a9.86 9.86 0 004.78 1.22h.01a9.86 9.86 0 006.99-17.93zM12.04 20.04a8.04 8.04 0 01-4.1-1.12l-.29-.17-3.12.82.82-3.04-.19-.31a8.04 8.04 0 01-1.24-4.3 8.04 8.04 0 018.08-8.04c2.15 0 4.17.84 5.69 2.36a8 8 0 012.35 5.68 8.04 8.04 0 01-8.04 8.12zm6.91-11.31a6.56 6.56 0 00-4.65-1.93 6.56 6.56 0 00-6.59 6.59c0 1.16.3 2.29.88 3.29l-1.08 3.95 4.04-1.06a6.53 6.53 0 003.11.79h.01a6.56 6.56 0 004.66-11.23l-.38-.4zM16.6 14.18c-.2-.1-1.18-.58-1.36-.65-.18-.07-.31-.1-.45.1s-.51.65-.63.79c-.11.13-.22.15-.42.05-.2-.1-.84-.31-1.6-.99-.59-.53-.99-1.18-1.1-1.38-.11-.2-.01-.31.09-.41.08-.08.2-.22.3-.33.1-.11.13-.19.2-.31.07-.13.03-.24-.02-.33-.05-.1-.45-1.08-.62-1.48-.16-.39-.32-.34-.45-.35h-.38c-.13 0-.33.05-.51.24-.18.2-.67.66-.67 1.6s.69 1.86.79 2c.1.13 1.36 2.08 3.3 2.92.46.2.82.32 1.1.41.46.15.88.13 1.21.08.37-.05 1.18-.48 1.35-.95.17-.47.17-.87.12-.95-.05-.08-.18-.13-.38-.23z"/></svg>
            WhatsApp
          </a>
          <a href="https://www.youtube.com/@IhabZaidiDev" target="_blank" class="inline-flex items-center gap-2 bg-white border border-zinc-200 px-5 py-3 rounded-full text-sm font-medium text-zinc-700 hover:border-zinc-300 hover:bg-zinc-50 transition">
            <svg class="w-4 h-4 text-red-600" fill="currentColor" viewBox="0 0 24 24"><path d="M23.5 12.04a3 3 0 00-2.1-2.12c-1.86-.5-9.4-.5-9.4-.5s-7.54 0-9.4.5A3 3 0 00.5 12.04a31 31 0 00-.5 5.96 3 3 0 002.1 2.12c1.86.5 9.4.5 9.4.5s7.54 0 9.4-.5a3 3 0 002.1-2.12 31 31 0 00.5-5.96zM9.75 16.5v-9l6.5 4.5z"/></svg>
            YouTube
          </a>
          <a href="https://www.linkedin.com/in/ihabzaidi/" target="_blank" class="inline-flex items-center gap-2 bg-white border border-zinc-200 px-5 py-3 rounded-full text-sm font-medium text-zinc-700 hover:border-zinc-300 hover:bg-zinc-50 transition">
            <svg class="w-4 h-4 text-[#0A66C2]" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.76 0-5 2.24-5 5v14c0 2.76 2.24 5 5 5h14c2.76 0 5-2.24 5-5v-14c0-2.76-2.24-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.27a1.5 1.5 0 110-3 1.5 1.5 0 010 3zm13 12.27h-3v-5.6c0-1.34-.48-2.26-1.7-2.26-.93 0-1.48.62-1.72 1.22-.09.22-.11.52-.11.83v5.81h-3s.04-9.44 0-11h3v1.56c.4-.61 1.11-1.49 2.7-1.49 1.97 0 3.45 1.29 3.45 4.06v6.87z"/></svg>
            LinkedIn
          </a>
        </div>

        <div class="mt-8 flex flex-wrap items-center gap-6 text-sm text-zinc-500 border-t border-zinc-100 pt-6">
          <div class="flex items-center gap-2">
            <svg class="w-4 h-4 text-zinc-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M12 21s7-5.5 7-11a7 7 0 10-14 0c0 5.5 7 11 7 11z"/><circle cx="12" cy="10" r="3"/></svg>
            Algeria • Remote
          </div>
          <div class="flex items-center gap-2">
            <svg class="w-4 h-4 text-zinc-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M16 21v-2a4 4 0 00-4-4H6a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg>
            Team Lead @ ItsourceOne
          </div>
          <div class="flex items-center gap-2">
            <svg class="w-4 h-4 text-zinc-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M21 11.5a8.38 8.38 0 01-1.9.5 3.5 3.5 0 001.53-1.9 7 7 0 01-2.2.85 3.5 3.5 0 00-6 2.4 10 10 0 01-7.2-3.6 3.5 3.5 0 001.08 4.7A3.4 3.4 0 014 14a3.5 3.5 0 003.14 2.45 7 7 0 01-5.16-1.43 3.5 3.5 0 002.76 1.74z"/><circle cx="12" cy="12" r="1"/></svg>
            Daily Streamer & Teacher
          </div>
        </div>
      </div>

      <!-- stats / card -->
      <div class="lg:col-span-5">
        <div class="bg-zinc-50 border border-zinc-100 rounded-[24px] p-6 sm:p-8">
          <div class="grid grid-cols-3 gap-4 text-center">
            <div class="bg-white border border-zinc-100 rounded-2xl p-4">
              <div class="text-2xl font-semibold text-zinc-900">13+</div>
              <div class="text-xs text-zinc-500 mt-1">Years<br/>in Dev</div>
            </div>
            <div class="bg-white border border-zinc-100 rounded-2xl p-4">
              <div class="text-2xl font-semibold text-zinc-900">13+</div>
              <div class="text-xs text-zinc-500 mt-1">Apps<br/>Shipped</div>
            </div>
            <div class="bg-white border border-zinc-100 rounded-2xl p-4">
              <div class="text-2xl font-semibold text-zinc-900">5+</div>
              <div class="text-xs text-zinc-500 mt-1">Years<br/>Lead @ ISO</div>
            </div>
          </div>

          <div class="mt-6 bg-white border border-zinc-100 rounded-2xl p-5">
            <div class="text-xs font-semibold tracking-widest text-zinc-400 uppercase">Current focus</div>
            <p class="mt-2 text-sm leading-6 text-zinc-600">
              Leading dev teams, shipping Vue/Nuxt & Flutter apps, Odoo + OWL modules — all with <span class="font-medium text-zinc-900">AI as daily assistant</span> — and streaming to help beginners start in digital. Strong <span class="font-medium text-zinc-900">problem solver</span>.
            </p>
            <div class="mt-4 flex flex-wrap gap-2">
              <span class="text-xs px-2.5 py-1 rounded-full bg-zinc-900 text-white">Vue.js</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-zinc-100 border border-zinc-200 text-zinc-700">Flutter</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-zinc-100 border border-zinc-200 text-zinc-700">Odoo</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-violet-50 border border-violet-200 text-violet-700">AI Daily</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-amber-50 border border-amber-200 text-amber-700">Problem Solving</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- STACK -->
  <section id="stack" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-10">
    <div class="flex items-end justify-between mb-6">
      <div>
        <h2 class="text-sm font-semibold tracking-widest uppercase text-zinc-400">Tech Stack</h2>
        <p class="mt-2 text-xl font-semibold tracking-tight text-zinc-900">Tools I use daily</p>
      </div>
      <p class="hidden sm:block text-sm text-zinc-500 max-w-xs text-right">Light, modern, production-ready stack — frontend to DevOps.</p>
    </div>
    <div class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-5 gap-3">
      <div v-for="t in techStack" :key="t.name" class="group border rounded-2xl px-3 py-4 text-center bg-white hover:shadow-sm transition" :class="t.color">
        <div class="text-sm font-semibold">{{ t.name }}</div>
        <div class="text-[11px] opacity-70 mt-1">{{ t.cat }}</div>
      </div>
    </div>
    <div class="mt-4 flex flex-wrap gap-2">
      <span class="inline-flex items-center gap-1.5 text-xs px-3 py-1.5 rounded-full bg-zinc-900 text-white">
        <span class="w-1.5 h-1.5 rounded-full bg-emerald-400"></span> Essentials in Cyber Security
      </span>
      <span class="inline-flex items-center gap-1.5 text-xs px-3 py-1.5 rounded-full bg-white border border-zinc-200 text-zinc-700">
        Reverse Engineering essentials
      </span>
      <span class="inline-flex items-center gap-1.5 text-xs px-3 py-1.5 rounded-full bg-pink-50 border border-pink-200 text-pink-700">
        n8n • Automation
      </span>
      <span class="inline-flex items-center gap-1.5 text-xs px-3 py-1.5 rounded-full bg-fuchsia-50 border border-fuchsia-200 text-fuchsia-700">
        AI — daily assistant
      </span>
    </div>
  </section>

  <!-- EXPERIENCE -->
  <section id="experience" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-10">
    <h2 class="text-sm font-semibold tracking-widest uppercase text-zinc-400">Experience • 13 Years in Dev</h2>
    <div class="mt-6 space-y-4">
      <!-- Current -->
      <div class="bg-white border border-zinc-200 rounded-[20px] p-6 sm:p-8">
        <div class="flex flex-col sm:flex-row sm:items-start justify-between gap-4">
          <div class="flex gap-4">
            <div class="w-11 h-11 rounded-xl bg-zinc-900 text-white flex items-center justify-center font-bold text-xs shrink-0">ISO</div>
            <div>
              <h3 class="font-semibold text-zinc-900">Senior Software Developer & Team Lead</h3>
              <p class="text-sm text-violet-600 font-medium">ItsourceOne • Full-time</p>
              <p class="mt-2 text-sm text-zinc-500 leading-6 max-w-2xl">
                As Team Lead my main role: <span class="font-medium text-zinc-700">manage projects, unblock devs, review code quality</span> and ensure delivery is <span class="font-medium text-zinc-700">scalable, maintainable and cost-efficient</span> — using AI daily to accelerate reviews & decisions.
              </p>
              <ul class="mt-4 space-y-2 text-sm text-zinc-600 list-disc list-inside">
                <li>Manage project scope, timeline & priorities — help devs daily on tasks & technical issues</li>
                <li>Check code quality via reviews & standards — enforce clean, scalable, maintainable architecture</li>
                <li>Design solutions to <span class="font-medium text-zinc-700">lower project cost</span> while keeping quality & performance</li>
                <li><span class="font-medium text-zinc-900">Great problem solver</span> — known for unblocking complex issues quickly</li>
                <li>Vue / React / Next + Flutter + Odoo/OWL + Express + Docker — from idea to production</li>
              </ul>
            </div>
          </div>
          <div class="sm:text-right shrink-0">
            <div class="inline-flex px-3 py-1 rounded-full bg-zinc-900 text-white text-xs font-medium">5 Years</div>
            <div class="text-xs text-zinc-400 mt-2">2019 — Present</div>
          </div>
        </div>
      </div>
      <!-- Early career -->
      <div class="bg-zinc-50 border border-zinc-200 rounded-[20px] p-6 sm:p-8">
        <div class="flex gap-4">
          <div class="w-11 h-11 rounded-xl bg-white border border-zinc-200 text-zinc-700 flex items-center justify-center font-bold text-xs shrink-0">.NET</div>
          <div class="flex-1">
            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2">
              <h3 class="font-semibold text-zinc-900">Software Developer — Early Career</h3>
              <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-zinc-200 text-zinc-600">2013 — 2019 • 8 Years</span>
            </div>
            <p class="mt-2 text-sm text-zinc-500 leading-6">
              In the dev world since ~2013. First production app shipped in <span class="font-medium text-zinc-700">2015 using .NET VB</span> — desktop/business apps, then moved to web & mobile modern stacks.
            </p>
            <div class="mt-3 flex flex-wrap gap-2">
              <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-zinc-200 text-zinc-700">.NET VB</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-zinc-200 text-zinc-700">VB.NET</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-zinc-200 text-zinc-700">→ Vue / React / Flutter</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- KEY ACHIEVEMENT -->
  <section id="achievement" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-6">
    <h2 class="text-sm font-semibold tracking-widest uppercase text-zinc-400">Key Achievement</h2>
    <div class="mt-4 bg-zinc-900 rounded-[20px] p-6 sm:p-8 text-white overflow-hidden relative">
      <div class="absolute -top-16 -right-16 w-64 h-64 bg-violet-600/20 rounded-full blur-3xl"></div>
      <div class="absolute -bottom-16 -left-16 w-64 h-64 bg-emerald-600/10 rounded-full blur-3xl"></div>
      <div class="relative flex flex-col lg:flex-row gap-6 items-start lg:items-center justify-between">
        <div class="flex gap-4">
          <div class="w-12 h-12 rounded-xl bg-white text-zinc-900 flex items-center justify-center shrink-0">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
          </div>
          <div>
            <h3 class="font-semibold text-white">Speech-to-Speech Translation — 20s → ~1s</h3>
            <p class="mt-2 text-sm leading-6 text-zinc-300 max-w-2xl">
              Solved critical performance bottleneck in speech-to-speech translation: cut latency from <span class="font-semibold text-white">20 seconds</span> to <span class="font-semibold text-emerald-400">~1 second or less</span> — <span class="text-white">20× faster</span>. Great problem-solving, audio pipeline optimization & AI integration.
            </p>
            <div class="mt-3 flex flex-wrap gap-2">
              <span class="text-xs px-2.5 py-1 rounded-full bg-white/10 border border-white/20 text-white">Problem Solving</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-emerald-500 text-white">20s → ~1s</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-white/10 border border-white/20 text-white">Speech-to-Speech</span>
              <span class="text-xs px-2.5 py-1 rounded-full bg-white/10 border border-white/20 text-white">Performance</span>
            </div>
          </div>
        </div>
        <div class="flex items-center gap-3 shrink-0">
          <div class="text-center bg-white/10 border border-white/10 rounded-2xl px-5 py-3">
            <div class="text-xs text-zinc-400 uppercase tracking-widest">Before</div>
            <div class="text-xl font-bold text-zinc-300 line-through">20s</div>
          </div>
          <svg class="w-5 h-5 text-emerald-400" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M13 5l7 7-7 7"/></svg>
          <div class="text-center bg-emerald-500 rounded-2xl px-5 py-3">
            <div class="text-xs text-white/80 uppercase tracking-widest">After</div>
            <div class="text-xl font-bold text-white">~1s</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- TEACHING & STREAMING -->
  <section id="teaching" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-6">
    <div class="bg-gradient-to-br from-violet-50 to-indigo-50 border border-violet-100 rounded-[20px] p-6 sm:p-7 flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4">
      <div class="flex gap-4">
        <div class="w-11 h-11 rounded-xl bg-violet-600 text-white flex items-center justify-center shrink-0">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M15 10l4.55-2.27A1 1 0 0121 8.6v6.8a1 1 0 01-1.45.89L15 14"/><rect x="1" y="6" width="14" height="12" rx="2"/></svg>
        </div>
        <div>
          <h3 class="font-semibold text-zinc-900">Daily Streaming & Teaching</h3>
          <p class="mt-1 text-sm leading-6 text-zinc-600 max-w-2xl">
            Based in <span class="font-medium text-zinc-900">Algeria</span> — I stream daily and teach people how to get started in the digital world: from first code to shipping real apps. I use <span class="font-medium text-zinc-900">AI as daily assistant</span> in professional work to ship faster and cleaner.
          </p>
          <div class="mt-3 flex flex-wrap gap-2">
            <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-violet-200 text-violet-700">Algeria</span>
            <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-violet-200 text-violet-700">Live Teaching</span>
            <span class="text-xs px-2.5 py-1 rounded-full bg-white border border-violet-200 text-violet-700">Digital Starter Guide</span>
            <span class="text-xs px-2.5 py-1 rounded-full bg-zinc-900 text-white">AI-assisted Dev</span>
          </div>
        </div>
      </div>
      <a href="https://www.youtube.com/@IhabZaidiDev" target="_blank" class="shrink-0 inline-flex items-center gap-2 bg-red-600 text-white px-5 py-2.5 rounded-full text-sm font-medium hover:bg-red-700 transition">
        <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M23.5 12.04a3 3 0 00-2.1-2.12c-1.86-.5-9.4-.5-9.4-.5s-7.54 0-9.4.5A3 3 0 00.5 12.04a31 31 0 00-.5 5.96 3 3 0 002.1 2.12c1.86.5 9.4.5 9.4.5s7.54 0 9.4-.5a3 3 0 002.1-2.12 31 31 0 00.5-5.96zM9.75 16.5v-9l6.5 4.5z"/></svg>
        YouTube @IhabZaidiDev
      </a>
    </div>
  </section>

  <!-- PROJECTS - Web -->
  <section id="projects" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-10">
    <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-3 mb-6">
      <div>
        <h2 class="text-sm font-semibold tracking-widest uppercase text-zinc-400">Selected Work</h2>
        <p class="mt-2 text-xl font-semibold tracking-tight text-zinc-900">Web Projects</p>
      </div>
      <p class="text-sm text-zinc-500">9 featured • E-commerce + Web Apps + Landing Pages • Live</p>
    </div>

    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-5">
      <article v-for="p in projects" :key="p.title" class="group bg-white border border-zinc-200 rounded-[20px] overflow-hidden hover:shadow-md transition flex flex-col">
        <div class="h-1.5 w-full bg-gradient-to-r" :class="p.accent"></div>
        <div class="p-6 flex flex-col flex-1">
          <div class="flex items-start justify-between gap-3">
            <div>
              <span class="inline-flex text-[10px] tracking-widest font-semibold uppercase px-2 py-1 rounded-full" :class="p.type === 'Web App' ? 'bg-sky-50 border border-sky-200 text-sky-700' : 'bg-violet-50 border border-violet-200 text-violet-700'">{{ p.type }}</span>
              <h3 class="mt-2 font-semibold text-zinc-900 leading-tight">{{ p.title }}</h3>
            </div>
            <span class="w-2 h-2 rounded-full bg-emerald-500 mt-3 shrink-0"></span>
          </div>
          <p class="mt-3 text-sm leading-6 text-zinc-500 flex-1">{{ p.desc }}</p>
          <div class="mt-4 flex flex-wrap gap-1.5">
            <span v-for="tag in p.tags" :key="tag" class="text-[11px] px-2.5 py-1 rounded-full bg-zinc-50 border border-zinc-200 text-zinc-600">{{ tag }}</span>
          </div>
          <div class="mt-5 flex gap-2">
            <a :href="p.url" target="_blank" rel="noopener" class="flex-1 inline-flex items-center justify-center gap-2 bg-zinc-900 text-white rounded-full py-2.5 text-sm font-medium hover:bg-black transition">
              Live
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M7 17L17 7"/><path d="M8 7h9v9"/></svg>
            </a>
            <a :href="p.url" target="_blank" rel="noopener" class="px-4 py-2.5 rounded-full border border-zinc-200 text-sm text-zinc-700 hover:bg-zinc-50 transition">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M15 3h6v6"/><path d="M10 14L21 3"/><path d="M18 13v6a2 2 0 01-2 2H5a2 2 0 01-2-2V8a2 2 0 012-2h6"/></svg>
            </a>
          </div>
        </div>
      </article>
    </div>
  </section>

  <!-- iOS APPS - 7 Apps on App Store -->
  <section id="apps" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-10">
    <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-3 mb-6">
      <div>
        <h2 class="text-sm font-semibold tracking-widest uppercase text-zinc-400">App Store • 7 Apps</h2>
        <p class="mt-2 text-xl font-semibold tracking-tight text-zinc-900">iOS Apps — Live on App Store</p>
        <p class="mt-1 text-sm text-zinc-500">Flutter • Native • All live with screenshots & icons</p>
      </div>
      <a href="https://apps.apple.com/us/developer/ech-chafai-kadri/id1789520174" target="_blank" class="hidden sm:inline-flex items-center gap-2 text-sm font-medium text-zinc-700 border border-zinc-200 rounded-full px-4 py-2 hover:bg-zinc-50 transition">
        View Developer Profile
        <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M7 17L17 7"/><path d="M8 7h9v9"/></svg>
      </a>
    </div>

    <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-5">
      <article v-for="app in iosApps" :key="app.name" class="group bg-white border border-zinc-200 rounded-[20px] p-5 hover:shadow-md hover:border-zinc-300 transition flex flex-col">
        <div class="flex gap-4">
          <img :src="app.icon" :alt="app.name" class="w-16 h-16 rounded-[14px] shadow-sm border border-zinc-100 object-cover shrink-0" loading="lazy" />
          <div class="min-w-0 flex-1">
            <h3 class="font-semibold text-zinc-900 leading-tight text-[14px] line-clamp-2">{{ app.name }}</h3>
            <p class="text-xs text-zinc-500 mt-1 line-clamp-1">{{ app.subtitle }}</p>
            <span class="inline-flex mt-2 text-[10px] tracking-widest font-semibold uppercase px-2 py-1 rounded-full bg-zinc-50 border border-zinc-200 text-zinc-600">{{ app.category }}</span>
          </div>
        </div>
        <p class="mt-4 text-[13px] leading-6 text-zinc-500 flex-1 line-clamp-3">{{ app.desc }}</p>
        <a :href="app.url" target="_blank" rel="noopener" class="mt-4 inline-flex items-center justify-center gap-2 w-full bg-zinc-900 text-white rounded-full py-2.5 text-sm font-medium hover:bg-black transition">
          <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.81-.91.65.03 2.47.26 3.64 1.98-.09.06-2.11 1.23-2.12 2.98.02 2.42 2.11 3.22 2.14 3.23-.02.06-.42 1.44-1.87 2.46zM12.36 2.18c.64-.83 1.07-1.98.93-3.13-1 .05-2.2.68-2.92 1.5-.65.75-1.22 1.95-.96 3.06 1.06.08 2.16-.54 2.95-1.43z"/></svg>
          View on App Store
        </a>
      </article>
    </div>
  </section>

  <!-- ANDROID APPS - Google Play -->
  <section id="android" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-8 sm:py-10">
    <div class="flex flex-col sm:flex-row sm:items-end justify-between gap-3 mb-6">
      <div>
        <h2 class="text-sm font-semibold tracking-widest uppercase text-zinc-400">Google Play • 3 Apps</h2>
        <p class="mt-2 text-xl font-semibold tracking-tight text-zinc-900">Android Apps — Live on Google Play</p>
        <p class="mt-1 text-sm text-zinc-500">IT Source One • Translation & Communication tools</p>
      </div>
      <a href="https://play.google.com/store/apps/developer?id=IT+Source+One" target="_blank" class="hidden sm:inline-flex items-center gap-2 text-sm font-medium text-zinc-700 border border-zinc-200 rounded-full px-4 py-2 hover:bg-zinc-50 transition">
        View on Google Play
        <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M7 17L17 7"/><path d="M8 7h9v9"/></svg>
      </a>
    </div>

    <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-5">
      <article v-for="app in androidApps" :key="app.name" class="group bg-white border border-zinc-200 rounded-[20px] p-5 hover:shadow-md hover:border-zinc-300 transition flex flex-col">
        <div class="flex gap-4">
          <img :src="app.icon" :alt="app.name" class="w-16 h-16 rounded-[14px] shadow-sm border border-zinc-100 object-cover shrink-0" loading="lazy" />
          <div class="min-w-0 flex-1">
            <h3 class="font-semibold text-zinc-900 leading-tight text-[14px] line-clamp-2">{{ app.name }}</h3>
            <p class="text-xs text-zinc-500 mt-1 line-clamp-1">{{ app.subtitle }}</p>
            <span class="inline-flex mt-2 text-[10px] tracking-widest font-semibold uppercase px-2 py-1 rounded-full bg-emerald-50 border border-emerald-200 text-emerald-700">{{ app.category }}</span>
          </div>
        </div>
        <p class="mt-4 text-[13px] leading-6 text-zinc-500 flex-1 line-clamp-3">{{ app.desc }}</p>
        <a :href="app.url" target="_blank" rel="noopener" class="mt-4 inline-flex items-center justify-center gap-2 w-full bg-emerald-600 text-white rounded-full py-2.5 text-sm font-medium hover:bg-emerald-700 transition">
          <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M3 20.5l17.5-8.5L3 3.5v8.3l11 0.2-11 .2v8.3z"/></svg>
          View on Google Play
        </a>
      </article>
    </div>
  </section>

  <!-- CONTACT - no form, direct contacts only -->
  <section id="contact" class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 pb-12">
    <div class="bg-zinc-900 rounded-[24px] p-6 sm:p-10 text-white overflow-hidden relative text-center">
      <div class="absolute -top-20 -right-20 w-64 h-64 bg-violet-600/20 rounded-full blur-3xl"></div>
      <div class="absolute -bottom-20 -left-20 w-64 h-64 bg-emerald-600/10 rounded-full blur-3xl"></div>
      <div class="relative max-w-3xl mx-auto">
        <h2 class="text-2xl sm:text-3xl font-semibold tracking-tight">Let’s build something clean.</h2>
        <p class="mt-3 text-sm leading-6 text-zinc-300 mx-auto max-w-xl">
          I’m Ihab — senior dev & team lead. If you need a fast, lightweight product with Vue, React, Flutter or Odoo — let’s talk.
        </p>

        <div class="mt-8 grid sm:grid-cols-2 gap-4 max-w-xl mx-auto">
          <a href="mailto:ihabeddinezaidi@gmail.com" class="group flex items-center gap-4 bg-white text-zinc-900 px-5 py-4 rounded-2xl text-left hover:bg-zinc-50 transition">
            <div class="w-11 h-11 rounded-xl bg-zinc-900 text-white flex items-center justify-center shrink-0">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M4 4h16v16H4z"/><path d="M4 7l8 6 8-6"/></svg>
            </div>
            <div>
              <div class="text-xs text-zinc-500 font-medium uppercase tracking-widest">Email</div>
              <div class="text-sm font-semibold">ihabeddinezaidi@gmail.com</div>
            </div>
          </a>
          <a href="https://wa.me/213797332534" target="_blank" class="group flex items-center gap-4 bg-emerald-500 text-white px-5 py-4 rounded-2xl text-left hover:bg-emerald-600 transition">
            <div class="w-11 h-11 rounded-xl bg-white/20 flex items-center justify-center shrink-0">
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M19.05 4.91A9.82 9.82 0 0012.04 2a9.86 9.86 0 00-8.5 14.86L2 22l5.26-1.38a9.86 9.86 0 004.78 1.22h.01a9.86 9.86 0 006.99-17.93zM12.04 20.04a8.04 8.04 0 01-4.1-1.12l-.29-.17-3.12.82.82-3.04-.19-.31a8.04 8.04 0 01-1.24-4.3 8.04 8.04 0 018.08-8.04c2.15 0 4.17.84 5.69 2.36a8 8 0 012.35 5.68 8.04 8.04 0 01-8.04 8.12zm6.91-11.31a6.56 6.56 0 00-4.65-1.93 6.56 6.56 0 00-6.59 6.59c0 1.16.3 2.29.88 3.29l-1.08 3.95 4.04-1.06a6.53 6.53 0 003.11.79h.01a6.56 6.56 0 004.66-11.23l-.38-.4zM16.6 14.18c-.2-.1-1.18-.58-1.36-.65-.18-.07-.31-.1-.45.1s-.51.65-.63.79c-.11.13-.22.15-.42.05-.2-.1-.84-.31-1.6-.99-.59-.53-.99-1.18-1.1-1.38-.11-.2-.01-.31.09-.41.08-.08.2-.22.3-.33.1-.11.13-.19.2-.31.07-.13.03-.24-.02-.33-.05-.1-.45-1.08-.62-1.48-.16-.39-.32-.34-.45-.35h-.38c-.13 0-.33.05-.51.24-.18.2-.67.66-.67 1.6s.69 1.86.79 2c.1.13 1.36 2.08 3.3 2.92.46.2.82.32 1.1.41.46.15.88.13 1.21.08.37-.05 1.18-.48 1.35-.95.17-.47.17-.87.12-.95-.05-.08-.18-.13-.38-.23z"/></svg>
            </div>
            <div>
              <div class="text-xs text-white/80 font-medium uppercase tracking-widest">WhatsApp</div>
              <div class="text-sm font-semibold">+213 797 332 534</div>
            </div>
          </a>
        </div>
        <p class="mt-4 text-xs text-zinc-500">
          <a href="tel:+213797332534" class="hover:text-white transition">Call</a>
          <span class="mx-2 opacity-30">•</span>
          <a href="https://wa.me/213797332534" target="_blank" class="hover:text-white transition">Chat on WhatsApp</a>
          <span class="mx-2 opacity-30">•</span>
          <a href="mailto:ihabeddinezaidi@gmail.com" class="hover:text-white transition">Send Email</a>
        </p>
      </div>
      <div class="mt-8 pt-6 border-t border-white/10 flex flex-col sm:flex-row items-center justify-between gap-3 text-xs text-zinc-400">
        <span>© {{ new Date().getFullYear() }} Ihab ZAIDI — Senior Software Developer</span>
        <div class="flex gap-4 items-center">
          <a href="https://www.youtube.com/@IhabZaidiDev" target="_blank" class="inline-flex items-center gap-1.5 hover:text-white transition">
            <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24"><path d="M23.5 12.04a3 3 0 00-2.1-2.12c-1.86-.5-9.4-.5-9.4-.5s-7.54 0-9.4.5A3 3 0 00.5 12.04a31 31 0 00-.5 5.96 3 3 0 002.1 2.12c1.86.5 9.4.5 9.4.5s7.54 0 9.4-.5a3 3 0 002.1-2.12 31 31 0 00.5-5.96zM9.75 16.5v-9l6.5 4.5z"/></svg>
            YouTube
          </a>
          <a href="https://www.linkedin.com/in/ihabzaidi/" target="_blank" class="inline-flex items-center gap-1.5 hover:text-white transition">
            <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24"><path d="M19 0h-14c-2.76 0-5 2.24-5 5v14c0 2.76 2.24 5 5 5h14c2.76 0 5-2.24 5-5v-14c0-2.76-2.24-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.27a1.5 1.5 0 110-3 1.5 1.5 0 010 3zm13 12.27h-3v-5.6c0-1.34-.48-2.26-1.7-2.26-.93 0-1.48.62-1.72 1.22-.09.22-.11.52-.11.83v5.81h-3s.04-9.44 0-11h3v1.56c.4-.61 1.11-1.49 2.7-1.49 1.97 0 3.45 1.29 3.45 4.06v6.87z"/></svg>
            LinkedIn
          </a>
          <a href="https://langaroo.co/" target="_blank" class="hover:text-white transition">Langaroo</a>
          <a href="https://invento-kappa.vercel.app/" target="_blank" class="hover:text-white transition">Invento</a>
        </div>
      </div>
    </div>
  </section>
</template>
