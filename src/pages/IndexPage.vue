<template>
  <q-page class="q-pa-lg bg-grey-2">
    <div class="row q-pb-md justify-between">
      <q-card class="q-pa-sm column justify-between col-3">
        <q-card-section class="text-h6"> Image Carousel </q-card-section>
        <ImageCarousel class="col" />
      </q-card>
      <q-card class="q-pa-md col q-mx-md">
        <DataTable />
      </q-card>
      <q-card class="q-pt-sm q-pl-sm col-3">
        <q-card-section class="text-h6">Satisfaction Slider</q-card-section>
        <q-card-section>
          <SatisfactionSlider />
        </q-card-section>
      </q-card>
    </div>
    <div class="row col-12 justify-between">
      <q-card class="col-5 q-pa-sm q-mr-md" style="height: 770px">
        <q-card-section class="text-h6"> Latest Reviews </q-card-section>
        <q-card-section>
          <q-scroll-area style="height: 600px">
            <LatestReviews />
          </q-scroll-area>
        </q-card-section>
      </q-card>
      <div class="col row justify-between">
        <div class="col-6 column q-pr-md q-pb-md">
          <q-card class="col row">
            <q-date
              class="col"
              title="Calendar"
              subtitle="Custom"
              first-day-of-week="1"
            />
          </q-card>
        </div>
        <div class="col-6 row q-pb-md">
          <q-card class="col">
            <q-editor v-model="editor" min-height="5rem"
          /></q-card>
        </div>
        <div class="col-6 row q-pr-md">
          <q-card class="col">
            <q-card-section class="text-h6">Chat Messages</q-card-section>
            <div style="width: 100%; max-width: 400px" class="q-pa-md">
              <q-chat-message
                name="me"
                avatar="https://cdn.quasar.dev/img/avatar2.jpg"
                :text="['hey, how are you?']"
                sent
                stamp="7 minutes ago"
              />
              <q-chat-message
                name="Jane"
                avatar="https://cdn.quasar.dev/img/avatar3.jpg"
                :text="['doing fine, how r you?']"
                stamp="4 minutes ago"
              />
            </div>
          </q-card>
        </div>
        <div class="col-6 row text-center">
          <q-card class="col">
            <q-time v-model="time" />
          </q-card>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import DataTable from "components/DataTable.vue";
import SatisfactionSlider from "src/components/SatisfactionSlider.vue";
import ImageCarousel from "src/components/ImageCarousel.vue";
import LatestReviews from "src/components/LatestReviews.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    DataTable,
    SatisfactionSlider,
    ImageCarousel,
    LatestReviews,
  },
  setup() {
    return {
      editor: ref("What you see is <b>what</b> you get."),
      time: ref("11:11"),
    };
  },
});
</script>
