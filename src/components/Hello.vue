<template>
  <div>
    <vue-ckeditor v-model="content" :config="config" @blur="onBlur($event)" @focus="onFocus($event)" />
  </div>
</template>

<script>
import { VueCkeditor } from 'vue-ckeditor2';

export default {
  name: 'hello',
  data() {
    return {
      content: '',
      config: {
        toolbar: [
          ['Bold', 'Italic', 'Underline', 'Strike', 'Subscript', 'Superscript']
        ],
        height: 300
      }
    };
  },
  methods: {
    onBlur(editor) {
      console.log(editor);
    },
    onFocus(editor) {
      console.log(editor);
    }
  },
  components: { VueCkeditor }
}
</script>

<style scoped></style>
