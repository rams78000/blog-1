<template>
    <div>
            {{ article.title }}
        <br>{{ article.body }}
        <br>{{ article.author }}
        
        <br> <div v-for="commentaire in article.comment" :key="commentaire.title">
        <br>{{commentaire.title}}
        <br>
        <br>{{commentaire.body}}
        <br>
        </div>
       <br>
    </div>
</template>

<script>
export default {
    props: 
        ['article','comment']
};

</script>