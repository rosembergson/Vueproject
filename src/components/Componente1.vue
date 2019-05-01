<template>
<div>
    <div class="componente1bg">
        <form action="POST">
            <label> Nome <input type="text" v-model="desenvolvedor.name"></label>
            <label> Sobrenome <input type="text" v-model="desenvolvedor.sobrenome"></label>
            <label> Email <input type="email" v-model="desenvolvedor.email"></label>
            <label> Idade <input type="text" v-model="desenvolvedor.idade"></label>
            <label> Gênero: 
                <input type="radio" name="gender" value="male"> Male
                <input type="radio" name="gender" value="female"> Female
            </label>
            <label>
            Cidade: 
                <select v-model="desenvolvedor.cidade">
                    <option value="Canindé">Canindé</option>
                    <option value="Caridade">Caridade</option>
                    <option value="Quixadá">Quixadá</option>
                    <option value="Jaguaretama">Jaguaretama</option>
                    <option value="Paramoti">Paramoti</option>
                    <option value="Barbalha">Barbalha</option>
                    <option value="Fortaleza">Fortaleza</option>    
                </select> </label>
        </form>
    </div>
</div>
</template>


<script>
export default {
    data(){
        return{
            desenvolvedor:{
                name:'',
                sobrenome:'',
                email:'',
                idade:'',
                genero:'',
                cidade:'',
            }
        }
    }
}
</script>

<style lang="scss">
    
</style>