# export-exel-rtl
To get Excel sheet output right to left

## Quick start

**npm i export-excel-rtl**
```javascript 
  import ExportExcelRtl from "export-excel-rtl";
  import Vue from "vue";

  Vue.use(ExportExcelRtl);
```
```
Several quick start options are available:

Download the latest release
Clone the repo: git clone https://github.com/sajjad101/export-exel-rtl
Install with npm: npm i export-excel-rtl
```

## Props 

```javascript 
props: {
    // mime type [xls, csv]
    type: {
      type: String,
      default: 'xls'
    },
    // Json to download
    data: {
      type: Array,
      required: false,
      default: null
    },
    // fields inside the Json Object that you want to export
    // if no given, all the properties in the Json are exported
    fields: {
      type: Object,
      default: () => null
    },
    // this prop is used to fix the problem with other components that use the
    // variable fields, like vee-validate. exportFields works exactly like fields
    exportFields: {
      type: Object,
      default: () => null
    },
    // Use as fallback when the row has no field values
    defaultValue: {
      type: String,
      required: false,
      default: ''
    },
    // Title(s) for the data, could be a string or an array of strings (multiple titles)
    header: {
      default: null
    },
    // Footer(s) for the data, could be a string or an array of strings (multiple footers)
    footer: {
      default: null
    },
    // filename to export
    name: {
      type: String,
      default: 'data.xls'
    },
    fetch: {
      type: Function
    },
    meta: {
      type: Array,
      default: () => []
    },
    worksheet: {
      type: String,
      default: 'Sheet1'
    },
    //event before generate was called
    beforeGenerate: {
      type: Function
    },
    //event before download pops up
    beforeFinish: {
      type: Function
    },
    // Determine if CSV Data should be escaped
    escapeCsv: {
      type: Boolean,
      default: true
    },
    // long number stringify
    stringifyLongNum: {
      type: Boolean,
      default: false
    }
  },
```
## Status
https://github.com/sajjad101/export-exel-rtl

https://www.npmjs.com/package/export-excel-rtl
