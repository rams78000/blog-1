<template>
<div>
    <h1>Hello Vue!</h1>
    <div v-for="article in articles" :key ="article.title">
        
        <Article :article='article'/>
        
        <!-- <Article :commentaire='article.comment'/> -->

    </div>    
</div>
</template>
<script>
import Article from "./Article";

export default {
    name:"Articles",
    
    data:()=>{
         
             return {
                articles :Articles,
                 
            
             } 
 
    
    },
    components: {
        Article, 

    }
   

}

const Articles = [

    {
        title:"Pourquoi les devs detestent PHP", 
        author:"angelus", 
        body: 'Le corps de l\'article',
        comment: [
            {
                title: 'commentaire 1',
                body: 'On a inter-VUE un devellopeur PHP  qui  nous a fait une synfo- NI devant l\'opera de paris À la différence des autres frameworks monolithiques, Vue a été conçu et pensé pour pouvoir être adopté de manière incrémentale. Le cœur de la bibliothèque est concentré uniquement sur la partie vue, et il est vraiment simple de l’intégrer avec d’autres bibliothèques ou projets existants. D’un autre côté, Vue est tout à fait capable de faire tourner des applications web monopages quand il est couplé avec des outils modernes et des bibliothèques complémentaires.'
            },
            {
                title: 'commentaire 2',
                body: 'La dissertation en cours d\'anglais est souvent redoutée par les élèves qui passent le bac. Il n\'est pas toujours facile de développer des idées et des arguments dans une langue étrangère. Il est donc impératif de bien se préparer et apprendre à organiser sa rédaction.'
            }
        ]
    },
    {
        title:"Pourquoi les devs aiment vue.js", 
        author:"alilevautour",
        body: 'Le corps de l\'article',
        comment: [
            {
                title: 'commentaire 1.1',
                body: 'coprs de comment 1'
            },
            {
                title: 'commentaire 2',
                body: 'coprs de comment 2'
            }
        ]
    },
    {
        title:"Pourquoi les devs aiment bien node.js ", 
        author:"david",      
        body: 'Le corps de l\'article',
        comment: [
            {
                title: 'commentaire 1.2',
                body: 'coprs de comment 1'
            },
            {
                title: 'commentaire 2',
                body: 'coprs de comment 2'
            }
        ]
    }

];
</script>
<style scoped>
h1{
    color: rgb(196, 12, 88)
}

</style>