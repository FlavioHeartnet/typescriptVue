<template>
    <div>
        <h1>Contador Classe</h1>
        <h2>{{ valor }}</h2>
        <h2>{{ParOuImpar}}</h2>
        <button @click="setValor(-1)">Dec</button>
        <button @click="setValor(1)">Inc</button>
    </div>
    
</template>


<script lang="ts">
import {Vue, Component, Prop} from 'vue-property-decorator'
import { extend } from 'vue/types/umd'

@Component
export default class ContadorClasse extends Vue{
    @Prop(Number) private readonly valorInicial?: number
    private valor:number = this.valorInicial || 0
    
    public setValor(delta:number){
        this.valor += delta
    }

    public get ParOuImpar(): string {
        return this.valor % 2 === 0 ? 'Par' : 'Impar'
    }
}
</script>

<style>

</style>