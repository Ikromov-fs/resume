<template>
  <div>
    <h1 class="text-[13px] md:text-[24px] md:font-bold">
      PROFESSIONAL EXPERIENCE
    </h1>
    <hr class="h-1 bg-black rounded-[2px]" />
    <div v-for="item in data" :key="item?.id">
      <h1 class="font-bold md:text-[25px]">{{ item?.job }}</h1>
      <div class="grid grid-cols-2">
        <div class="flex items-end">
          <img :src="building" alt="icon" class="w-[20%] max-w-[40px]" />
          <span class="sx:text-[13px] sm:text-[13px] lg:text-[20px]">{{
            item?.place
          }}</span>
        </div>
        <div class="grid grid-cols-2">
          <div class="flex items-center gap-1">
            <img :src="date" alt="icon" class="sx:w-[22%] max-w-[25px]" />
            <p
              class="sx:text-[8px] sm:text-[12px] xl:text-[16px] flex justify-end"
            >
              {{ item?.date }}
            </p>
          </div>
          <div class="flex items-center gap-1">
            <img :src="located" alt="icon" class="w-[20%] max-w-[18px]" />
            <p
              class="sx:text-[9px] sm:text-[12px] xl:text-[16px] flex justify-end"
            >
              {{ item?.laktation }}
            </p>
          </div>
        </div>
        <div class="md:gap-1 flex items-center">
          <img
            :src="link"
            alt="icon"
            class="sx:w-[22%] max-w-[25px] rotate-[-45deg]"
          />
          <a :href="item?.link" class="font-bold md:text-[16px]"
            >{{ item?.linkName }}|</a
          >
          <span class="sx:text-[10px] md:text-[15px]">{{
            item?.linkNameAfter
          }}</span>
        </div>
      </div>
      <ul class="list-disc mt-2">
        <li v-for="itemChild in item?.texts" class="md:text-[1.3rem]">
          {{ itemChild?.dataText }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script setup>
import building from "../../assets/svg/building.svg";
import located from "../../assets/svg/located.svg";
import date from "../../assets/svg/date.svg";
import link from "../../assets/svg/link.svg";
const data = [
  {
    id: 1,
    job: "Backend Engineer",
    place: "Fireart Studio",
    date: "09.2022-present",
    laktation: "Warsaw, Poland",
    link: "http://algaritm.uz/",
    linkName: "fireart.studio",
    linkNameAfter: "full-time (remote)",
    texts: [
      {
        id: 1,
        dataText:
          "Developed and launched a web application using React and Node.js, enabling users to create personalized daily web digests with content from sources such as Reddit, Hacker News, Twitter, and more. View the live project at usedigest.com",
      },
      {
        id: 2,
        dataText:
          "Integrated user authentication through social media platforms including Google, Facebook, and Twitter using OAuth APIs, providing users with a seamless and secure login experience.",
      },
      {
        id: 3,
        dataText:
          "Optimized data storage and retrieval by implementing a single table design for AWS DynamoDB in the project.",
      },
      {
        id: 4,
        dataText:
          "Implemented comprehensive unit and integration testing for the project using Jest, resulting in improved code quality, reduced bug occurrence, and increased development efficiency.",
      },
    ],
  },
];
</script>
<style scoped></style>
