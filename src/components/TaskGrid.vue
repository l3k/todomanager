<template>
    <div>
        <template>
            <v-layout justify-center>
                <v-flex xs3>
                    <div v-if="tasks.length">                        
                        <task v-for="(task, i) in tasks" :key="task.name" :task=task @taskDeleted="$emit('taskDeleted', i)" @taskStateChanged="$emit('taskStateChanged', i)"></task>
                    </div>
                    <h1 v-else>Sua vida esta em dia 😁</h1>
                </v-flex>
            </v-layout>
        </template>
    </div>
</template>

<script>
    import Task from './Task'
    export default {
        components: {
            Task,
        },
        props: {
            tasks: {
                type: Array,
                required: true
            },
        },
        data() {
            return {

            }
        },
        methods: {
        },
    };
</script>

<style>
</style>
