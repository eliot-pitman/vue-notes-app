<script>
export default {
  props: ["note", "selectedNotId"],
  methods: {
    selectNote: function (note) {
      this.$emite("selectNote", note);
    },
  },
};
</script>

<template>
  <div class="note-selector" v-bind:class="{ active: selectedNoteID === note.id }" @click="selectNote">
    <p class="note-selector-title">{{ note.body }}</p>
    <p class="note-selector-timestamp">{{ note.timestamp }}</p>
  </div>
</template>
