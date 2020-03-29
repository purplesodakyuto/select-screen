<template src="./template.html"></template>
<style src="./style.scss" lang="scss" scoped>
</style>

<script>
import CharacterFrame from "@/components/CharacterFrame/component.vue";
import Character from "@/services/Character.js";
export default {
  components: {
    "character-frame": CharacterFrame
  },
  data() {
    return {
      data: ""
    };
  },
  computed: {
    characterList: function() {
      return Character;
    },
    link: function() {
      if (this.data == "") {
        return `url(${this.characterList[0].imageURL})` ;
      } else {
        return `url(${this.data.imageURL})`;
      }
    }
  },
  methods: {
    hoverImage(data) {
      this.data = data;
    },
    showName(data) {
      this.data = data;
    }
  }
};
</script>