<template>
    <div id="addForm">
        <form @submit.prevent="handleAdd">
            <div class="form-group">
                <label for="id">Id</label>
                <input v-model="product.id" type="text" class="form-control" id="id">
            </div>

            <div class="form-group">
                <label for="categoryId">Category Id</label>
                <input v-model="product.categoryId" type="text" class="form-control" id="categoryId">
            </div>

            <div class="form-group">
                <label for="productName">Ürün Adı</label>
                <input v-model="product.productName" type="text" class="form-control" id="productName">
            </div>

            <div class="form-group">
                <label for="quantityPerUnit">Açıklama</label>
                <input v-model="product.quantityPerUnit" type="text" class="form-control" id="quantityPerUnit">
            </div>

             <div class="form-group">
                <label for="unitPrice">Fiyat</label>
                <input v-model="product.unitPrice" type="text" class="form-control" id="unitPrice">
            </div>

             <div class="form-group">
                <label for="unitsInStock">Stok</label>
                <input v-model="product.unitsInStock" type="text" class="form-control" id="unitsInStock">
            </div>
            <br>
            <button type="submit" class="btn btn-sm btn-success">Kaydet</button>
        </form>
    </div>
</template>

<script>


export default{
    name:"product-add",
    data(){
        return{
            product:{id:"",categoryId:"",productName:"",quantityPerUnit:"",unitPrice:"",unitsInStock:""}
        }
    },
    methods:{
        handleAdd(){
            this.$emit("add:product",this.product)
        }
    }       

}
</script>

<style scoped>
#addForm{
    margin-left:100px;
    text-align: left;
    font-family: 'Times New Roman', Times, serif;
    
}
</style>
