<template>
    <div>
        <h4>This is a test compound</h4>
        <p>My name is {{name}}</p>
        <p>My age is {{age}}</p>
        <input type="text" v-model="name">
        <button @click="getName()">Click me</button>
        <ul>
            <li v-for="name in people" :key="name">{{name}}</li>
        </ul>

    </div>
</template>

<script>
    export default {
       data() {
           return {
               name: "",
               age: "40",
               people: ['Chinenye', 'Victory', 'Victor', 'Kelechi']
           }
       },

       mounted () {
           //this.getName();
       },
       
       methods: {
           getName() {
               if (this.name == ''){
                   alert('Enter a name')
             } else {
                 this.people.push(this.name);
                 this.name = '';
                   
                }

            //    this.people.push(this.name);
            //    this.name = '';
            //    this.people.shift('New name');
            //    alert(this.name)
               
           }
       },
    }
</script>

<style scoped>

</style>