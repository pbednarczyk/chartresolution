<script>
import Vue from "vue";

import "@carbon/styles/css/styles.css";

import "@carbon/charts/styles.css";
import chartsVue from "@carbon/charts-vue";

// IBM Plex should either be imported in your project by using Carbon
// or consumed manually through an import
import "../ibm-plex-font.css";

Vue.use(chartsVue);

export default {
  name: "Chart",
  components: {},
  data() {
    return {
      data: [
        {
          group: "Target",
          date: "2022-01-01T00:00:00Z",
          value: 0,
        },
        {
          group: "Target",
          date: "2022-12-31T00:00:00Z",
          value: 1000,
        },
        {
          group: "Angielski",
          value: 50,
          date: "2022-01-06T15:38:39Z",
        },
        {
          group: "Angielski",
          value: 60,
          date: "2022-02-08T15:38:39Z",
        },
        {
          group: "Angielski",
          value: 66,
          date: "2022-02-09T15:38:39Z",
        },
        {
          group: "Angielski",
          value: 400,
          date: "2022-03-03T15:38:39Z",
        },
        {
          group: "Angielski",
          value: 502,
          date: "2022-03-05T15:38:39Z",
        },
        {
          group: "Angielski",
          value: 571,
          date: "2022-06-04T15:38:39Z",
        },
      ],
      options: {
        title: "Angielski 1000 słów w rok",
        axes: {
          bottom: {
            mapsTo: "date",
            scaleType: "time",
          },
          left: {
            mapsTo: "value",
            title: "Conversion rate",
            scaleType: "linear",
          },
        },
        curve: "curveLinear",
        height: "700px",
        resizable: true,
        animations: true,
      },
    };
  },
  template: "<ccv-line-chart :data='data' :options='options'></ccv-line-chart>",
};
</script>
  