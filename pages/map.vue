<template>
  <mindmap :nodes="nodes" :connections="connections" :editable="true" />
</template>

<script>
import Vue from "vue";
import VueMindmap from "vue-mindmap";
import "vue-mindmap/dist/vue-mindmap.css";
Vue.use(VueMindmap);
alert("hogea");
export default {
  name: "MindmapTest",
  data() {
    return {
      nodes: [
        { text: "テスト1", fx: 100, fy: 100, nodes: [{ text: "テストサブ1" }] },
        {
          text: "テスト2",
          fx: 200,
          fy: 200,
          nodes: [{ text: "テストサブ2-1" }, { text: "テストサブ2-2" }],
        },
        { text: "テスト3", fx: 300, fy: 300 },
      ],
      connections: [{ source: "テスト1", target: "テスト2" }],
    };
  },
};
</script>

