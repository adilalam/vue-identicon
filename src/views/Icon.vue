<template>
  <div class="about">
    <h1>My Identicon Generator</h1>

    <div>
      Input:
      <input type="text" @input="onInput" />
    </div>

    <div>
      Output:
      <div id="placeholder"></div>
    </div>
  </div>
</template>

<script>
const jdenticon = require('jdenticon');

export default {
  name: 'Icon',
  data() {
    return {
      msg: '',
    };
  },
  methods: {
    onInput(e) {
      const placeholder = document.getElementById('placeholder');
      placeholder.innerHTML = jdenticon.toSvg(e.target.value, 200);
    },
  },
};
</script>
