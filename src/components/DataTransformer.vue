<template>
<div>
    <diagram :model="model" width="80%" height="600"></diagram>
    <br/>
    <b-button variant="outline-primary" v-on:click="next()">Next >></b-button>
</div>
</template>
<script>
import { Diagram } from 'vue-diagrams';

export default {
  data() {

    //sample file
    const diagramModel = new Diagram.Model();

    const node1 = diagramModel.addNode("ADDRESS", 300, 100, 200, 120);
    node1.addInPort("street");
    node1.addInPort("huouse number");
    node1.addInPort("postal code");
    node1.addInPort("city");

    const node2 = diagramModel.addNode("GEOMETRY", 300, 300, 200, 120);
    node2.addInPort("latitude");
    node2.addInPort("longitude");

    const node3 = diagramModel.addNode("BAN", -100, 100, 200, 320);
    node3.addOutPort("nom_commune");
    node3.addOutPort("id");
    node3.addOutPort("numero");

    node3.addOutPort("nom_voie");
    node3.addOutPort("code_postal");
    node3.addOutPort("code_insee");

    node3.addOutPort("x");
    node3.addOutPort("y");
    node3.addOutPort("lat");

    node3.addOutPort("lon");

    node3.addOutPort("libelle_acheminement");
    node3.addOutPort("nom_afnor");
    node3.addOutPort("source_position");
    node3.addOutPort("source_nom_voie");

    node3.color = "#cc6600";

    // diagramModel.addLink(node2OutPort, inPort);
    // diagramModel.addLink(node3OutPort, inPort);

    return {
      model: diagramModel
    };
  },
  methods:{
    next(){
      console.log('BEXT IOS CLICKED');
    }
  },
  components: {
    Diagram
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
