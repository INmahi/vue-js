<template>
  <div class="content">
    <card>
      <template slot="header">
        <div class="row">
        <div class="col-md-3">
        <h3 class="title">Export Overview</h3></div>
        <div class="col-md-2"><button type="button" class="btn btn-block"><!---->View a Quick demo</button></div>
        <div class="col-md-5 pr-md-1 text-left">
            <base-input 
                        placeholder="Track by Container number"
                        class="">
            </base-input>
            
          </div>
          <div class="col-md-1"><base-button to="/export_detail" type="Save" fill>TRACK</base-button></div>
        <p class="category"></a></p>
      </div>
      
      </template>

      <div class="row">
        <a href="#" class="button col-md-2"><div class="" style="border-bottom: 1px; border-bottom-color:black;border-bottom-style:solid;">Shipments</div></a>
        <a href="#" class="button col-md-2"><div class="">ETA Changes</div></a>
        <a href="#" class="button col-md-2"><div class="">Unconfirmed Bookings</div></a>
        <a href="#" class="button col-md-2"><div class="">Documents</div></a>

        <base-button type="Save" fill>Detail page</base-button>
      </div>

      <div class="col-12">
        <card class="card-plain">
          <template slot="header">
                <h4 class="card-title"> Data</h4>
                <p class="category"> </p>
              </template>
          <div class="table-full-width table-responsive text-left">
            <base-table :title="table2.title" :sub-title="table2.subTitle" :data="table2.data"
                        :columns="table2.columns">
                        
            </base-table>
          </div>
        </card>
      </div>
      <!--<div class="row">
        <div v-for="icon in icons" class="font-icon-list col-lg-2 col-md-3 col-sm-4 col-xs-6 col-xs-6">
          <div class="font-icon-detail">
            <i class="tim-icons" :class="[`${icon}`]"></i>
            <p>{{ icon }}</p>
          </div>
        </div>
      </div>-->
    </card>
  </div>
</template>
<script>

import {
  Card,
  BaseInput
} from "@/components/index";

import BaseButton from '@/components/BaseButton';
import BaseTable from "@/components/BaseTable";

const tableColumns = ["BLNumber",
        "From",
        "To",
        "Vessel", "Cargo"];
const tableData = [
{
          "id": 1,
          "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
        },
  {
    id: 2,
    "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
  },
  {
    id: 3,
    "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
  },
  {
    id: 4,
    "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
  },
  {
    id: 5,
    "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
  },
  {
    id: 6,
    "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
  },
  {
    id: 7,
    "blnumber": "221233",
          "vessel": "Container",
          "from": "China",
          "to": "UAE",
          "cargo": "ship"
  }
];



export default{
  components:{
    Card,
    BaseInput,
    BaseButton,
    BaseTable
  },
  data(){
    return{
      table2: {
        title: "Table on Plain Background",
        columns: [...tableColumns],
        data: [...tableData]
      },
      icons: [
        "icon-alert-circle-exc",
        "icon-align-center",
        "icon-align-left-2",
        "icon-app",
        "icon-atom",
        "icon-attach-87",
        "icon-badge",
        "icon-bag-16",
        "icon-bank",
        "icon-basket-simple",
        "icon-bell-55",
        "icon-bold",
        "icon-book-bookmark",
        "icon-double-right",
        "icon-bulb-63",
        "icon-bullet-list-67",
        "icon-bus-front-12",
        "icon-button-power",
        "icon-camera-18",
        "icon-calendar-60",
        "icon-caps-small",
        "icon-cart",
        "icon-chart-bar-32",
        "icon-chart-pie-36",
        "icon-chat-33",
        "icon-check-2",
        "icon-cloud-download-93",
        "icon-cloud-upload-94",
        "icon-coins",
        "icon-compass-05",
        "icon-controller",
        "icon-credit-card",
        "icon-delivery-fast",
        "icon-email-85",
        "icon-gift-2",
        "icon-globe-2",
        "icon-headphones",
        "icon-heart-2",
        "icon-html5",
        "icon-double-left",
        "icon-image-02",
        "icon-istanbul",
        "icon-key-25",
        "icon-laptop",
        "icon-light-3",
        "icon-link-72",
        "icon-lock-circle",
        "icon-map-big",
        "icon-minimal-down",
        "icon-minimal-left",
        "icon-minimal-right",
        "icon-minimal-up",
        "icon-mobile",
        "icon-molecule-40",
        "icon-money-coins",
        "icon-notes",
        "icon-palette",
        "icon-paper",
        "icon-pin",
        "icon-planet",
        "icon-puzzle-10",
        "icon-pencil",
        "icon-satisfied",
        "icon-scissors",
        "icon-send",
        "icon-settings-gear-63",
        "icon-settings",
        "icon-wifi",
        "icon-single-02",
        "icon-single-copy-04",
        "icon-sound-wave",
        "icon-spaceship",
        "icon-square-pin",
        "icon-support-17",
        "icon-tablet-2",
        "icon-tag",
        "icon-tap-02",
        "icon-tie-bow",
        "icon-time-alarm",
        "icon-trash-simple",
        "icon-trophy",
        "icon-tv-2",
        "icon-upload",
        "icon-user-run",
        "icon-vector",
        "icon-video-66",
        "icon-wallet-43",
        "icon-volume-98",
        "icon-watch-time",
        "icon-world",
        "icon-zoom-split",
        "icon-refresh-01",
        "icon-refresh-02",
        "icon-shape-star",
        "icon-components",
        "icon-triangle-right-17",
        "icon-button-pause",
        "icon-simple-remove",
        "icon-simple-add",
        "icon-simple-delete"
      ],
    }
  }
};
</script>
<style>
</style>
