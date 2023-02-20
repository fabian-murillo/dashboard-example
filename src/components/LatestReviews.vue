<template>
  <q-timeline color="secondary">
    <q-timeline-entry
      title="First Review"
      subtitle="February 22, 1986"
      avatar="https://cdn.quasar.dev/img/avatar3.jpg"
      body="Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
    />

    <q-timeline-entry
      title="Second Review"
      subtitle="February 21, 1986"
      avatar="https://cdn.quasar.dev/img/avatar1.jpg"
      body="Aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
    />

    <q-timeline-entry
      title="Third Review"
      subtitle="February 22, 1986"
      avatar="https://cdn.quasar.dev/img/avatar2.jpg"
      body="
      Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur."
    />

    <q-timeline-entry
      title="Event Title"
      subtitle="February 22, 1986"
      :body="body"
    />

    <q-timeline-entry
      title="Event Title"
      subtitle="February 22, 1986"
      color="orange"
      icon="done_all"
      :body="body"
    />

    <q-timeline-entry
      title="Event Title"
      subtitle="February 22, 1986"
      :body="body"
    />

    <q-timeline-entry
      title="Event Title"
      subtitle="February 22, 1986"
      :body="body"
    />
  </q-timeline>
</template>

<script>
export default {
  name: "LatestReviews",
  setup() {
    return {};
  },
};
</script>
