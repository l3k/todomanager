<template>
    <div>
        <v-card class="mt-3"  :class="stateClass">  
            <v-card-title primary-title>
                <div style="display: flex">
                    <h3 class="">{{ task.name }}</h3>
                </div>
            </v-card-title>
            <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn icon>
                    <v-icon>delete</v-icon>
                </v-btn>
            </v-card-actions>
        </v-card>
    </div>
</template>

<script>
export default {
    props: {
        task: {
            type: Object,
            required: true 
        },
    },

    computed: {
        stateClass() {
            return {
                pending: this.task.pending,
                done: !this.task.pending,
            }
        }
    },
}
</script>

<style>
    .pending {
        background-color: #C62828 !important;
        border-color: #C62828 !important;
    }
    
    .done{
        background-color: #2e7d32 !important;
        border-color: #2e7d32 !important;
    }
</style>
