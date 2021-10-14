<template>
  <div class="backdrop">
    <h1>hello world Modal</h1>
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>{{ header }}</h1>
      <p>
        {{ text }}
      </p>

      <p>Button Text...{{buttonTxt}}</p>
      <button @click="changeimg('image1')">Change Image</button>
      <button @click="changeimg('image2')">Change Back</button>
    </div>
  </div>
</template>

<script>
  export default {
    props: ["header", "text", "theme"],
    data() {
      return {
        buttonTxt: "default"
      }
    },
    methods: {
      changeimg: function(val) {
        this.buttonTxt = val
        alert("Clicked on " + this.buttonTxt )
      }
    }
  };

</script>


<style>
  .modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: #fff;
    border-radius: 10px;
  }
  .backdrop {
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
  }
  .modal h1 {
    color: darkmagenta;
  }

  .modal.sale {
    background: maroon;
    color: white;
  }
  .modal.sale h1 {
    color: white;
  }
</style>