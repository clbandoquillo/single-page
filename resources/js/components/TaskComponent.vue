<template>
    <div>
        <button class="btn btn-primary btn-block">Add New Task</button>
        <table class="table">
            <thead>
                <tr>
                    <th scope="col">id</th>
                    <th scope="col">Name</th>
                    <th scope="col">Body</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>My Task</td>
                    <td>Description of Task</td>
                    <td><button class="btn btn-info">Edit</button></td>
                    <td><button class="btn btn-danger">Delete</button></td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {

        data(){
            return{
                task:{
                    name: '',
                    body: ''
                },

                tasks: [],
                uri: 'http://127.0.0.1:8000/'
            }
        },

        methods: {

            loadTask(){

                axios.get(this.uri).then(response => {

                });
            }
        },

        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
