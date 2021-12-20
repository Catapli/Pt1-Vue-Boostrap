<template>
    <div class="row">
            <div class="col-sm-6 col-md-4 col-lg-4">
                <form id="new-prod" @submit.prevent="putInDB">
                    <fieldset>
                        <legend>Nuevo producto</legend>
                        <label for="newprod-id">Id del producto:</label>
                            <input type="text" class="form-control"  disabled required min="1" step="1"><br>
                        <div class="form-group">
                            <label for="newprod-name">Nombre: </label>
                            <input type="text" class="form-control" v-model="newProduct.name" id="newprod-name">
                        </div>
                        <div class="form-group">
                            <label for="newprod-price">Precio: </label>
                            <input type="number" class="form-control"  v-model.number="newProduct.price" id="newprod-price">
                        </div>
                        <div class="form-group">
                            <label for="newprod-units">Units: </label>
                            <input type="number" class="form-control"  v-model.number="newProduct.units" id="newprod-units">
                        </div>
                        <br>
                        <button type="submit" class="btn btn-default btn-primary">Añadir</button>
                        <button type="reset" class="btn btn-secondary">Reset</button>

                        <!-- Aquí los inputs y botones del form -->
                    </fieldset>
                </form>
            </div>
    </div>
</template>

<script>
import Api from '../services/Api.js'
export default {
    name: "appForm",
    data(){
        return{
            newProduct : {
                name: "",
                price: "",
                units: ""

            }
        }
    },
    methods:{
        putInDB(){
            if(this.newProduct.name === ""){
                alert("Debes Colocar un nombre")
            }else if(this.newProduct.price <= 0){
                alert("Debes colocar un precio")
            }else if (this.newProduct.units <= 0){
                alert("Debes colocar unas unidades")
            }else{
                Api.products.create(this.newProduct)
            }

        }
    }
}
</script>