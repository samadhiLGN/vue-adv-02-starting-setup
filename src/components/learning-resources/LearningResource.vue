<template>
    <base-card>
    <li>
      
            <header>
                <h3>{{ title }}</h3>
                <the-button mode="flat">Delete</the-button>
            </header>
      
        <p>{{ description }}</p>
        <nav>
            <a :href="link">View Resourece</a>
        </nav>
    </li>
</base-card>
  
</template>


<script>
import TheButton from '../UI/BaseButton.vue'
export default{
  components: { TheButton },
    props: ['title', 'description', 'link']
}
    

</script>
<style scoped>
    li {
    margin: auto;
    max-width: 40rem;
    }

    header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    }

    h3 {
    font-size: 1.25rem;
    margin: 0.5rem 0;
    }

    p {
    margin: 0.5rem 0;
    }

    a {
    text-decoration: none;
    color: #ce5c00;
    }

    a:hover,
    a:active {
    color: #c89300;
    }
</style>