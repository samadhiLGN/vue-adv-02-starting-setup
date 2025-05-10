<template>
    <base-card>
        <base-button @click="setSelectedTab('stored-resources')">Sotored Resources</base-button>
        <base-button @click="setSelectedTab('add-resource')">Add Resource</base-button>
    </base-card>
    <component :is="setSelectedTab"></component>
</template>


<script>
import StoredResources from './StoredResources.vue';
import AddResource from '.AddResource.vue';

export default {
    components: {
       StoredResources,
       AddResource 
    },
    data(){
        return {
            selectedTab: 'stored-resources'
        };
    },
    methods: {
        setSelectedTab(tab) {
            this.selectedTab = tab;
        }
       
    }
}
</script>
