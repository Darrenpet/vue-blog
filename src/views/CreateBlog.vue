<template>
  <form @submit.prevent="createBlog" class="form neu-border">
    <h2 class="form-heading">Create a blog</h2>
    <input
      class="form-input neu-border-inset"
      type="text"
      v-model="title"
      placeholder="Title"
    />
    <input
      class="form-input neu-border-inset"
      type="text"
      v-model="img"
      placeholder="Blog Image"
    />
    <textarea
      class="form-input neu-border-inset"
      type="text"
      v-model="body"
      placeholder="Body"
    ></textarea>
    
    <button type="submit" class="form-btn neu-border">Create Blog</button>
    

    
  </form>
</template>
<script>
export default {
  data() {
    return {
      title: "",
      body: "",
      img: "",
    };
  },
  methods: {
    createBlog() {
     console.log(this.title, this.body, this.img)
    },
  },
};
</script>
<style>
.neu-border {
  border-radius: 30px;
  background: #f5f5f5;
  box-shadow: 8px 8px 15px #e4e4e4, -8px -8px 15px #ffffff;
}
.neu-border-inset {
  border-radius: 30px;
  background: #f5f5f5;
  box-shadow: inset 8px 8px 15px #e4e4e4, inset -8px -8px 15px #ffffff;
}

.form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 40px;
  gap: 20px;
  width: 100%;
  max-width: 600px;
  margin-inline: auto;
}

.form-heading {
  text-align: center;
  text-transform: uppercase;
}

.form-input,
.form-btn {
  border: none;
  outline: none;
  padding: 20px;
}

.form-btn {
  cursor: pointer;
  transition: all 0.1s linear;
}

.form-btn:hover {
  transform: scale(1.05);
}

.form-social-login {
  display: flex;
  justify-content: space-between;
}

.form-social-btn {
  width: 45%;
  color: #333;
}
</style>
