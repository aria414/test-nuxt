<template>
  <div>
    <h1>hello Index</h1>
    <Modal :header="header" :text="text" theme="sale" />

  </div>

</template>

<script>
export default {
  data() {
    return {
      title: "Sample Form",
      header: "Order Form",
      text: "Place your order here"
    };
  },
  methods: {
    handleClick() {
      console.log(this.$refs.myinput);
      this.$refs.myinput.classList.add("active");
      this.$refs.myinput.focus();
    }
  }
};

</script>
