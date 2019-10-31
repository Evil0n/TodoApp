<template>
  <div>
    <h1>Create an Event, {{ user.name }}</h1>
    <p>This event was create by {{ user.id }}</p>
    <p>{{ getEventByID(2) }}</p>
  </div>
</template>

<script>
import { mapState, mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["getEventByID"]),
    ...mapState(["user", "categories"])
    /*  mapState({
                user: "user",
                categories: "categories"
              })   я не понял как он это вот так сократил */
  }
};
</script>

<style scoped></style>
