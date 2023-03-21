<template>
    <div class="cards">
        <img :src="character.image" :alt="character.name">
        <div class="cards__item">
            <h3 class="nombre">{{ character.name }}</h3>
        </div>
        <div class="status">
            <span :class="
                character.status == 'Alive'? 'alive' : 
                character.status== 'Dead' ? 'dead': 'default'">
             </span>
            <span  class="informacion">
            {{character.status}} - {{character.species}}
            </span>
        </div>
        
        <div class="origin">
        <span class="informacion">
            Origin:
            {{character.origin.name}}
        </span>
        </div>
        <div class="location">
            <span class="informacion">
                Location:
                {{character.location.name}}
            </span>
        </div>
    </div>
    
</template>

<script>
    export default {
        props: ['character']
    }
</script>
<style>
:root{
    --bg-card:#333;
    --bg-body:#222;
    --text-orange:rgb(224, 125, 12);
    --text-grey:#777;
    --blanco:#fff;
}
.cards {
    display: flex;
    flex-direction: column;
    gap: .5rem;
    background-color: var(--bg-card);
    border-radius: 20px;
    box-shadow: 0 0 10px 1px var(--bg-body);
    overflow: hidden;
    cursor: pointer;
    transition: transform 200ms ease-in-out;
    height: 100%;
    
}
.cards:hover{
    transform: scale(1.05);
}
.nombre:hover{
    color: var(--text-orange);
}
.informacion{
    color: var(--text-grey);
    margin-left: .5rem;
    
}
.nombre{
    margin-bottom: 0.5rem;
    margin-left: .5rem;
    color: var(--blanco);
    cursor: pointer;
}
.status{
    display: flex;
    align-items: center;
    
}
.location{
    margin-bottom: .6rem;
}
span:first-child{
    width: 10px;
    height: 10px;
    border-radius: 50%;
    
}
.alive{
    margin-left: .5rem;
    background-color: green;
}
.dead{
    margin-left: .5rem;
    background-color: red;
}
.default{
    margin-left: .5rem;
    background-color: white;
}

</style>