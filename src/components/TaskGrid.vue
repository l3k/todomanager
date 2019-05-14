<template>
    <div>
        <template>
            <v-layout justify-center>
                <v-flex xs2>
                    <task v-for="task in tasks" :key="task.name" :task=task></task>
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
        }
    };
</script>

<style>
</style>
