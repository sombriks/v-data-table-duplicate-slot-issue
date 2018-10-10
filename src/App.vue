<template>
  <div id="app" app>
    <HelloWorld>
      <tr slot="header">
        <th>Dessert</th>
        <th class="hidden-sm-and-down">Calories</th>
        <th class="hidden-sm-and-down">Fat</th>
        <th class="hidden-sm-and-down">Carbs</th>
        <th>Protein</th>
        <th>Iron</th>
      </tr>
      <tr slot="item" slot-scope="{item}">
        <td>{{ item.name }}</td>
        <td class="text-xs-right">{{ item.calories }}</td>
        <td class="text-xs-right hidden-sm-and-down">{{ item.fat }}</td>
        <td class="text-xs-right hidden-sm-and-down">{{ item.carbs }}</td>
        <td class="text-xs-right hidden-sm-and-down">{{ item.protein }}</td>
        <td class="text-xs-right">{{ item.iron }}</td>
      </tr>
    </HelloWorld>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
