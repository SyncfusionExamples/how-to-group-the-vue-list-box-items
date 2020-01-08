<template>
  <div class = 'controls'>
  <div class = 'listbox_parent'>
    <ejs-listbox :dataSource='dataItem' :fields='dataFields'
    allowDragAndDrop='true' scope='combined-list'>
    </ejs-listbox>
  </div>
  <div class = 'listbox_child'>
    <ejs-listbox :dataSource='dataItemChild' 
    :fields='dataFieldsChild' allowDragAndDrop='true' 
    scope='combined-list'>
    </ejs-listbox>
  </div>
  </div>
</template>

<script>
import Vue from "vue";
import {ListBoxPlugin} from "@syncfusion/ej2-vue-dropdowns";
Vue.use(ListBoxPlugin);
export default Vue.extend({
  data: function() {
    return {
      dataItem: [
        { Name: 'Cabbage', Id: 'item1', Category: 'Leafy and Salad'},
        { Name: 'Pumpkins', Id: 'item2', Category: 'Leafy and Salad' },
        { Name: 'Spinach', Id: 'item3', Category: 'Leafy and Salad'},
        { Name: 'Green bean', Id: 'item4', Category: 'Beans' },
        { Name: 'Horse gram', Id: 'item5', Category: 'Beans'},
        { Name: 'Chickpea', Id: 'item6', Category: 'Beans'}
        ],
      dataFields: { text: 'Name', value: 'Id', groupBy: 'Category' },
      dataItemChild: [
        { Name: 'Watercress', Id: 'item1', Category: 'Leafy and Salad' },
        { Name: 'Beet Greens', Id: 'item2', Category: 'Leafy and Salad' },
        { Name: 'Romaine Lettuce', Id: 'item3', Category: 'Leafy and Salad' },
        { Name: 'Black Beans', Id: 'item4', Category: 'Beans' },
        { Name: 'Soybeans', Id: 'item5', Category: 'Beans' },
        { Name: 'Lentils', Id: 'item6', Category: 'Beans' }
      ],
      dataFieldsChild: { text: 'Name', value: 'Id', groupBy: 'Category'}
    };
  }
});
</script>




<style>
@import url(https://cdn.syncfusion.com/ej2/material.css);

.controls {
  display: inline-block;
  width: 100%;
}

.listbox_parent {
 width: 300px;
 margin-top: 15%;
 margin-bottom: 15%;
 margin-left: 15%;
 margin-right: 5%;
 float: left;
}

.listbox_child {
  width: 300px;
  margin-top: 15%;
  float: left;
}

</style>
