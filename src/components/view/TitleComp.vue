<template>
  <h1 id="article_title">{{ title }}</h1>
  <div class="article_tags" v-for="(tag, i) in tags" :key="i">{{ tag }}</div>
  <hr id="article_hr" />
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    tags: {
      type: Array,
    },
  },
};
</script>

<style>
#article_title {
  font-size: 2rem;
  margin-bottom: 1rem;
  word-wrap: keep-all;
}
.article_tags {
  display: inline-block;
  margin: 0.4rem;
  background-color: #f5f5f5;
  padding: 0.2rem 0.4rem;
  width: fit-content;
  border-radius: 5px;
  font-size: 0.8rem;
  font-weight: 300;
  letter-spacing: 0.04rem;
}
#article_hr {
  margin: 3rem auto;
  border: none;
  opacity: 0.5;
  border-bottom: 1px solid #a3a3a3;
}

/* CSS for sub-Pages in '@/components/view/~View'
 * Use <article> tag to format main text
*/
.article {
  line-height: 1.6;
  width: 100%;
  word-wrap: keep-all;
}
article > img {
  max-width: 90%;
  max-height: 40vh;
  margin: 2rem auto;
  display: block;
}
article > img.img-shadow {
  box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
}
article > h3 {
  margin-top: 5rem;
  color: #0f766e;
}
article p ~ ul > li {
  line-height: 2rem;
}
article a {
  color: #000;
  text-decoration: underline;
  font-style: normal;
}
article p ~ ul > li > span {
  font-weight: 300;
  color: #a3a3a3;
}

@media (max-width: 640px) {
  #article_title {
    font-size: 1.4rem;
    margin: 0px 0.4rem 1rem 0.4rem;
  }
  article {
    font-weight: 500;
    margin: 0px -0.8rem;
    word-break: break-all;
  }
}
</style>
