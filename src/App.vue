<script setup>

import { ref } from "vue";

//navbar

import brand from '@/assets/img/brand.svg'

let isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
}
//navbar

//header
import MainHeader from '@/components/LandingPageHeader.vue'

//main
//kerjasama
import img1 from "@/assets/img/partner/img-1.png";
import img2 from "@/assets/img/partner/img-2.png";
import img3 from "@/assets/img/partner/img-3.png";
import img4 from "@/assets/img/partner/img-4.png";
import img5 from "@/assets/img/partner/img-5.png";
import img6 from "@/assets/img/partner/img-6.png";

const partners = ref([
  { id: 0, url: img1 },
  { id: 1, url: img2 },
  { id: 2, url: img3 },
  { id: 3, url: img4 },
  { id: 4, url: img5 },
  { id: 5, url: img6 },
]);
//blog
import img1_blog from "@/assets/img/blog/img1.png";
import img2_blog from "@/assets/img/blog/img2.png";
import img3_blog from "@/assets/img/blog/img3.png";
import img4_blog from "@/assets/img/blog/img4.png";
import profile from "@/assets/img/blog/profile_pict.png";

const events = ref([
  {
    id: 0,
    url: img1_blog,
    title: "Quality Assurance",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  },
  {
    id: 1,
    url: img2_blog,
    title: "Project Manager",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  },
  {
    id: 2,
    url: img3_blog,
    title: "Development Operational",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  },
  {
    id: 3,
    url: img4_blog,
    title: "Fullstack Developer",
    jenisKelas: "Live Class",
    durasi: "3 Bulan",
    peminat: {
      url: profile,
      peminat: "3000+"
    }
  }
])
//cerita sukses
import img1_cerita from '@/assets/img/cerita/img-1.png';
import img2_cerita from '@/assets/img/cerita/img-2.png';
import img3_cerita from '@/assets/img/cerita/img-3.png';

const stories = ref([
  {
    id: 0,
    img: img1_cerita,
    name: "Syhabudin Ahmad",
    job: "Project Manager Solutionlabs",
    story: "Program SISTEM top markotop. Selama belajar cara penyampaian dan arahan mentor unik selain itu mentor juga siap membantu kami jika ada kesulitan."
  },
  {
    id: 1,
    img: img2_cerita,
    name: "Annastasya KW",
    job: "Project Manager Solutionlabs",
    story: "Dulu sebelum belajar tentang PM di SISTEM sering kesulitan buat manage project. Setelah ikut bootcamp SISTEM jadi tau gimana biar project itu bisa selesai dan achive."
  },
  {
    id: 2,
    img: img3_cerita,
    name: "Tasya WA",
    job: "Quality Assurance Solutions",
    story: "Kemarin waktu belajar coding di sini enak banget. Kita di kelas bener-bener dibimbing dari nol (0) sama mentor dari pembelajarannya juga gampang dipahami."
  }
])
//main

//footer
import logo from '@/assets/img/sistem_white.svg';
import instagram from '@/assets/img/instagram_logo.svg';
import phone_logo from '@/assets/img/phone.svg';
import mail_logo from '@/assets/img/mail.svg';
//footer
</script>

<template>
<!--main navbar-->
  <nav class="flex flex-row items-center justify-between w-full px-5 py-3 md:px-32 md:py-5">
    <img :src="brand" alt="">

    <ul class="flex-row items-center justify-between hidden text-base md:flex font-inter text-slate-800">
      <li class="mr-8 text-blue-600"><a href="#">Home</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">Blog</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">About Us</a></li>
      <li class="mr-8 hover:text-blue-600"><a href="#">Contact Us</a></li>
    </ul>

    <button
      class="hidden py-2 font-bold text-white transition-all duration-500 bg-blue-700 border border-blue-700 rounded-full md:block font-sen hover:text-blue-700 hover:bg-transparent px-7">
      Contact Us
    </button>
    <button @click="toggleMenu" class="flex flex-col gap-1 py-2 font-bold text-white md:hidden font-sen">
      <div class="h-[2px] w-[20px] bg-black"></div>
      <div class="h-[2px] w-[20px] bg-black"></div>
      <div class="h-[2px] w-[20px] bg-black"></div>
    </button>
  </nav>
  <div v-if="isOpen" class="absolute z-10 w-full bg-slate-700">
    <ul>
      <li class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter"><a
          href="">Home</a></li>
      <li class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter"><a
          href="">Blog</a></li>
      <li class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter"><a
          href="">About</a></li>
      <li class="px-4 py-2 text-base font-normal leading-relaxed border-b text-slate-300 border-slate-600 font-inter"><a
          href="">Contact Us</a></li>
    </ul>
  </div>
  <div v-if="isOpen" class="absolute opacity-50 w-svw h-[100vh] bg-slate-800"></div>

<!--main header-->
  <MainHeader />

<!--main-->
<!--content kerjasama-->
  <div class="flex flex-col items-center justify-between w-full px-5 py-5 md:px-32 md:py-16">
    <h1 class="mb-5 text-xl font-semibold text-center md:leading-relaxed font-montserrat md:text-3xl">
      Berbagai Mitra Untuk Mendukung Ekosistem Digital SISTEM
    </h1>
    <div class="flex flex-row items-center justify-between w-full overflow-visible"> 
      <div class="block p-4" v-for="partner in partners" :key="partner.id">
        <img :src="partner.url" alt="Partner Logo" />
      </div>
    </div>
  </div>

<!--landing blog-->
<div class="flex flex-col w-full px-5 py-5 mt-5 md:px-32 md:pt-16">
    <div class="">
      <h1 class="text-xl font-semibold text-center md:text-3xl mb-7 font-montserrat">Pilih Pengalaman Event Terbaik
      </h1>
      <p class="mb-5 -mt-4 text-xs font-normal text-center md:text-sm font-inter text-slate-500 ">Cari berbagai macam
        event
        teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya</p>
    </div>

    <div class="grid items-center justify-between w-full grid-cols-2 gap-4 md:gap-6 md:flex md:flex-row">
      <div v-for="event in events" :key="event.id"
        class="flex flex-col overflow-hidden rounded-lg shadow-lg shadow-slate-400">
        <div class="w-full">
          <img :src="event.url" :alt="event.title">
        </div>
        <div class="w-full p-5 text-slate-500">
          <div class="">
            <h4
              class="text-base font-semibold leading-5 md:text-lg font-inter line-clamp-2 md:line-clamp-1 text-slate-800">
              {{
                event.title
              }}
            </h4>
            <p class="mb-5 text-xs font-normal md:text-sm font-inter">{{ event.jenisKelas }} {{ event.durasi }}</p>
          </div>
          <div class="flex flex-row items-center justify-start gap-2 mb-4 md:gap-3">
            <img :src="event.peminat.url" :alt="event.peminat.peminat" class="w-1/2">
            <p class="text-xs font-semibold md:text-sm font-inter md:text-md text-slate-800">{{ event.peminat.peminat }}
            </p>
          </div>

          <a href="#" class="text-xs text-blue-600 md:text-md">Daftar Sekarang →</a>
        </div>
      </div>
    </div>
  </div>

<!--landing about-->
  <div class="flex flex-col items-center justify-between w-full px-5 py-5 md:px-32 md:pt-16">
    <div class="flex flex-row w-full h-5">
      <div class="w-1/4 bg-white"></div>
      <div class="w-1/2 bg-yellow-400"></div>
      <div class="w-1/4 bg-blue-500"></div>
    </div>
    <div class="w-full flex flex-col md:flex-row items-start justify-around gap-8 bg-[#F4F0F8] py-20 px-14">
      <div class="flex flex-col w-full gap-3 text-center md:left md:w-1/2">
        <h3 class="font-semibold text-slate-800 font-inter text-md">TENTANG KAMI</h3>
        <h2 class="text-lg md:text-[28px] leading-snug font-semibold font-montserrat">Mulai Karir Sukses Anda di
          Teknik
          Perangkat Lunak dengan SISTEM BOOTCAMP</h2>
        <p class="text-sm leading-relaxed text-slate-400 font-inter">Lorem ipsum dolor sit amet, consectetur adipiscing
          elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
      </div>
      <div class="flex flex-col w-full gap-3 text-center md:left md:w-1/2">
        <h3 class="font-semibold text-slate-800 font-inter text-md">VISI KAMI</h3>
        <h2 class="text-lg text-[22px] leading-normal font-semibold font-montserrat">Membuat Peradaban Teknologi yang
          Terbaik untuk seluruh dunia</h2>
        <p class="text-sm leading-relaxed text-slate-400 font-inter">Lorem ipsum dolor sit amet, consectetur adipiscing
          elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
          exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      </div>
    </div>
  </div>

<!--cerita sukses-->
  <div class="flex flex-col w-full px-5 py-5 md:px-32 md:py-16">
    <div class="flex flex-col w-full">
      <h1 class="text-3xl font-semibold text-center mb-7 font-montserrat">Cerita Sukses Peserta</h1>
      <p class="mb-5 -mt-4 text-xs font-normal text-center md:text-sm font-inter text-slate-500">Cari berbagai macam
        event
        teknologi terbaik yang diadakan oleh komunitas dan di dukung oleh banyak perusahaan besar lainnya</p>
    </div>

    <div class="flex flex-col items-center justify-between w-full gap-5 mt-5 md:flex-row">
      <div v-for="story in stories" :key="story.id" class="p-8 pb-10 bg-white rounded-md shadow-md shadow-slate-400">
        <div class="flex flex-row items-center justify-start gap-3 mb-8">
          <img :src="story.img" :alt="story.name" class="size-16">
          <div class="flex flex-col gap-1">
            <h3 class="text-lg font-semibold">{{ story.name }}</h3>
            <p class="text-xs font-normal text-slate-500 font-inter">{{ story.job }}</p>
          </div>
        </div>
        <p class="text-sm font-normal leading-relaxed text-slate-800 font-inter">{{ story.story }}</p>
      </div>
    </div>
  </div>

<!--join us-->
  <div class="flex flex-col items-center justify-center w-full gap-3 px-5 py-5 md:gap-6 md:px-32 md:py-16">
    <h1
      class="max-w-2xl text-xl font-semibold leading-relaxed text-center md:text-3xl mb-7 font-montserrat line-clamp-2">
      Gabung
      Jadi Talenta Digital Terbaik Bersama SISTEM</h1>
    <p
      class="mb-5 -mt-4 text-xs font-normal leading-relaxed text-center md:text-sm font-inter text-slate-500 line-clamp-2 max-w-96">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>

    <button
      class="py-3 font-bold text-white transition-all duration-500 bg-blue-700 border border-blue-700 rounded-lg font-sen hover:text-blue-700 hover:bg-transparent px-7">
      Daftar Sekarang</button>
  </div>

<!--footer-->
  <footer
    class="flex flex-col items-start justify-between w-full gap-8 px-5 py-5 md:gap-0 md:flex-row md:px-32 md:py-16 bg-blue-950">
    <div class="flex flex-col w-full gap-5 md:gap-8 md:w-1/3">
      <img :src="logo" alt="wtf" class="w-1/4 md:w-1/2 fill-white">
      <div class="address">
        <h5 class="text-xl font-semibold leading-relaxed font-inter text-slate-300">Jogja Office</h5>
        <p class="text-base font-normal leading-relaxed font-inter text-slate-400">Jl. Kresna. Gamping kidul,
          Amberketawang, Kec.Gamping, Kabupaten Sleman, DIY 55294</p>
      </div>
      <div class="address">
        <h5 class="text-xl font-semibold leading-relaxed font-inter text-slate-300">Jakarta Office</h5>
        <p class="text-base font-normal leading-relaxed font-inter text-slate-400">Cibis Nine Building Lantai 11 Jl. TB
          Simatupang No.2, Jakarta Selatan</p>
      </div>
    </div>
    <div class="flex justify-between w-full md:px-0 md:justify-around">
      <div class="flex flex-col w-1/3 gap-4 md:gap-7">
        <h5 class="text-xl font-semibold leading-relaxed text-slate-200 font-inter">Bootcamp</h5>
        <ul class="flex flex-col gap-2 md:gap-5 font-inter text-slate-400">
          <li><a href="#">Devops</a></li>
          <li><a href="#">Quality Assurance</a></li>
          <li><a href="#">Full Stack Developer</a></li>
          <li><a href="#">Project Manager</a></li>
        </ul>
      </div>
      <div class="flex flex-col w-1/3 gap-4 md:gap-7">
        <h5 class="text-xl font-semibold leading-relaxed text-slate-200 font-inter">SISTEM</h5>
        <ul class="flex flex-col gap-2 md:gap-5 font-inter text-slate-400">
          <li><a href="#">Tentang Kami</a></li>
          <li><a href="#">Events</a></li>
          <li><a href="#">FAQ</a></li>
        </ul>
      </div>
    </div>
    <div class="flex flex-col w-full gap-4 mg:gap-7 md:w-1/5">
      <h5 class="text-xl font-semibold leading-relaxed text-white font-inter">Ikuti kami</h5>
      <div class="flex items-center justify-center w-8 h-8 p-1 border-2 border-blue-900 rounded-md">
        <img :src="instagram" alt="Instagram Logo" class="size-[80%] fill-white">
      </div>
      <div class="flex gap-3">
        <img :src="phone_logo" alt="lol" class="fill-green-600 stroke-green-600 size-6">
        <a href="#" class="text-sm font-normal font-inter text-slate-400">+62 857 4270 8990</a>
      </div>
      <div class="flex gap-3">
        <img :src="mail_logo" alt="lol" class="fill-green-600 stroke-green-600 size-6">
        <a href="#" class="text-sm font-normal font-inter text-slate-400">chrissetiawan1402@student.uns.ac.id</a>
      </div>
    </div>
  </footer>

</template>
