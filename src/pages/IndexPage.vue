<template>
  <q-page class="q-pa-lg bg-grey-2">
    <div class="row q-pb-md justify-around">
      <q-card
        style="min-height: 300px"
        class="q-pa-sm column col-xs-12 col-sm-12 col-md-grow col-lg-grow q-mb-xs-md q-mb-md-none q-mr-md-md q-mr-lg-none"
      >
        <q-card-section class="text-h6"> Image Carousel </q-card-section>
        <ImageCarousel class="col" />
      </q-card>
      <q-card
        class="col-xs-12 col-sm-12 col-md-col order-md-last order-lg-none col-lg-5 q-mt-md-md q-mt-lg-none q-mx-md-md"
      >
        <DataTable />
      </q-card>
      <q-card
        class="col-xs-12 col-sm-12 col-md-grow col-lg-grow q-mt-xs-md q-mt-sm-md q-mt-md-none"
      >
        <q-card-section class="text-h6">Satisfaction Slider</q-card-section>
        <q-card-section>
          <SatisfactionSlider />
        </q-card-section>
      </q-card>
    </div>

    <div class="row">
      <q-card
        class="col-xs-12 col-sm-12 col-md-6 q-mr-md-md q-mr-lg-none"
        style="height: 770px"
      >
        <q-card-section class="text-h6"> Latest Reviews </q-card-section>
        <q-card-section>
          <q-scroll-area style="height: 600px">
            <LatestReviews />
          </q-scroll-area>
        </q-card-section>
      </q-card>
      <div
        class="flex flex-end col-xs-12 col-sm-12 col-md-5 col-lg-6 q-mt-xs-md q-mt-md-none"
      >
        <div class="row">
          <q-date
            class="col-xs-12 col-sm-12 col-md-6"
            title="Calendar"
            subtitle="Custom"
            first-day-of-week="1"
          />
          <q-editor
            class="col-xs-12 col-sm-12 col-md-6 q-mt-xs-md q-mt-md-none"
            v-model="editor"
          />

          <q-card
            class="col-xs-12 col-sm-12 col-md-6 q-mt-xs-md q-mt-md-none text-center"
          >
            <q-time v-model="time" />
          </q-card>
          <q-card class="col-xs-12 col-md-6 q-mt-xs-md q-mt-md-none">
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
