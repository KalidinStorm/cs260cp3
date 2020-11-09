<template>
    <div>

        <form>
            <div class="form-group form-check" id="userbox">
                <div class="checkboxbox">
                    <input type="checkbox" v-model="user.captainamerica" id="captainamerica" class="form-check-input" /> <label class="form-check-label" for="captainamerica">Captain America</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.ironman" id="ironman" class="form-check-input" /> <label class="form-check-label" for="ironman">Iron man</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.hulk" id="hulk" /> <label class="form-check-label" for="hulk">Hulk</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.thor" id="thor" /> <label class="form-check-label" for="thor">Thor</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.hawkeye" id="hawkeye" /> <label class="form-check-label" for="hawkeye">Hawk Eye</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.blackwidow" id="blackwidow" /> <label class="form-check-label" for="blackwidow">Black Widow</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.blackpanther" id="blackpanther" /> <label class="form-check-label" for="blackpanther">Black Panther</label><br />
                </div><div class="checkboxbox">
                    <input type="checkbox" v-model="user.drstrange" id="drstrange" /> <label class="form-check-label" for="drstrange">Dr. Strange</label><br />
                </div>
            </div>
        </form>
        <ProductList :products="products" />
    </div>

</template>

<script>
    import ProductList from "../components/ProductList.vue"
    export default {
        
        
        components: {
            ProductList,
            
        },
        data() {
            return {
                user: {
                    captainamerica: false,
                    ironman: false,
                    hulk: false,
                    thor: false,
                    hawkeye: false,
                    blackwidow: false,
                    blackpanther: false,
                    drstrange: false,
                }
            }
        },
        computed: {
            products() {
                return this.$root.$data.products.filter(product => (product.captainamerica == this.user.captainamerica || product.captainamerica == true)
                    && (product.ironman == this.user.ironman || product.ironman == true)
                    && (product.hulk == this.user.hulk || product.hulk == true)
                    && (product.thor == this.user.thor || product.thor == true)
                    && (product.hawkeye == this.user.hawkeye || product.hawkeye == true)
                    && (product.blackwidow == this.user.blackwidow || product.blackwidow == true)
                    && (product.blackpanther == this.user.blackpanther || product.blackpanther == true)
                    && (product.drstrange == this.user.drstrange || product.drstrange == true)
                );
            },
            
        },
        methods: {
            
        }
    }


</script>

<style>
    #userbox {
        background-color: #bebebe;
        display: flex;
        align-items: center;
        justify-content: center;
        border: 1px solid #5D6063;
        border-radius: 20px;
    }

    .checkboxbox {
        background-color: #cecece;
        border: 1px solid #5D6063;
        border-radius: 20px;
        padding: 10px;
        margin: 5px;
    }
</style>