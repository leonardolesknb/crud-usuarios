<template>
    <header>
        <!-- Posso usar o router.go direto ao invés das opções descritas abaixo / Vou usar o router.go(-1) para que sempre que eu estiver em um rota X e eu clicar em voltar
        eu vou voltar uma rota antes -->
        <a href="#" class="voltar" @click.prevent="$router.go(-1)">
            <img src="@/assets/arrow.svg" alt="Voltar">
        </a>
        
        <div>
            <a href="#" class="usuario" title="Clique para deslogar" @click.prevent="deslogar">
                Leo ✌️
            </a>
        </div>
    </header>
</template>

<script>
export default {
    name: 'BaseMenu',
    // Metodos são funções que eu utilizo pra facilitar/dar funcionalidade para o meu componente ou seja
    methods:{
            // this faz com que neste projeto procuremos determinada coisa.
            // console.log(this.$route) Route faz eu pegar todas os parametros/informações que eu tenho na url atual que eu estou
            // this.$router me da funções das modificações das rotas
            // Usando this.$router.push, consigo redirecionar o usuário para outra página
        deslogar(){
            console.log("deslogar");
        }
    }

}
</script>

<style scoped>
    header{
        padding:15px 20px;
        min-height:75px;
        border-bottom: 1px solid #ececec;
        display:flex;
        align-items: center;
        justify-content: space-between;
    }
    .voltar{
        background-color: #f7f7f7;
        display: flex;
        align-items: center;
        justify-content: center;
        width:45px;
        height:45px;
        border-radius:50%;
    }
    .voltar img{
        width:20px;
    }
    .usuario{
        background-color: rgba(58,85,221,.2);
        border-radius:5px;
        padding:15px 20px;
        font-size:14px;
        color: #3a55dd;
    }
</style>