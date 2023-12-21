<!-- eslint-disable max-len -->
<!-- eslint-disable vuejs-accessibility/label-has-for -->
<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Form @submit="onSubmit" v-slot="{ errors }">
      {{ errors }}
      <div class="mb-3">
        <label for="email" class="form-label">Email</label>
        <Field id="email" name="email" type="email" class="form-control" placeholder="請輸入Email" rules="email|required" v-model="user.email" :class="{ 'is-invalid': errors['email']}"></Field>
        <error-message name="email" class="invalid-feedback"></error-message>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
  </Form>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Home',
  components: {
    HelloWorld,
  },
  data() {
    return {
      user: {
        email: '',
      },
    };
  },
  methods: {
    onSubmit() {
      console.log(this.user);
    },
  },
  created() {
    console.log(this);
  },
};
</script>
