<template>
  <footer class="footer">
    <div class="footer-section" v-for="(section, index) in sections" :key="index">
      <h3>{{ section.title }}</h3>
      <ul v-if="section.title !== 'Blog'">
        <li v-for="(item, i) in section.items" :key="i">{{ item }}</li>
      </ul>
      <div v-else>
        <div class="blog-post" v-for="(post, i) in section.posts" :key="i">
          <img :src="post.image" alt="Post image" />
          <div>
            <h4>{{ post.title }}</h4>
            <p>{{ post.date }}</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>

export default {
  data() {
    return {
      sections: [
        {
          title: 'About',
          items: ['Masterstudy is Education WordPress theme featured by Learning Management System (LMS) for online education. Developed by StylemixThemes'],
        },
        {
          title: 'Contact',
          items: ['USA, Callifornia 20, First Avenue, Callifornia', '+1 212 458 300 32', '+1 212 375 24 14', 'info@masterstudy.com'],
        },
        {
          title: 'Pages',
          items: ['Blog', 'Home', 'Typography', 'Courses', 'Shortchhuts', 'membership'],
        },
        {
          title: 'Blog',
          posts: [
            {
              image: 'src/assets/img/photo-1490376840453-5f616fbebe5b-50x50.jpeg',
              title: 'Those Other College Expenses You Aren`t Thinking About',
              date: '12 Maggio 2023',
            },
            {
              image: 'src/assets/img/photo-1517520287167-4bbf64a00d66-75x75.jpeg',
              title: 'Our main target is to “Developing Yourself as a Leader”',
              date: '11 Maggio 2023',
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">

@import '../scss/Footer.scss';


</style>
