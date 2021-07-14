<template>
  <div id="app">
    <b-excel
      :fetch="getItems"
      header="excelHeader"
      stringifyLongNum="stringifyLongNum"
      :fields="fileds"
      type="xls"
      name="fileName"
    >
    <button>export exel</button>
      <!-- can put your button hear for export exel -->
    </b-excel>
  </div>
</template>

<script>
  import BExcel from "./components/BExcel.vue";

  export default {
    name: "Export Excel",
    components: {
      BExcel,
    },

    data() {
      return {
        // thats data want to export excel
        data: [
          { name: "jun", age: 12 },
          { name: "mohammad", age: 13 },
          { name: "lucy", age: 20 }
        ],
        //create your json fileds
        json_fileds: {
          ["name"]: "name",
          ["age"]: {
            field: "age",
            callback: (value) => {
              return value
            }
          }
        }
      }
    },
    methods: {
      getItems() {
        return this.data
      }
    }
  }
</script>
