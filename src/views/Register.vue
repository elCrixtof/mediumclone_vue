<template>
    <div class="auth-page">
        <div class="container-page">
            <div class="row">
                <div class="col-md-6 offset-md-3 col-xs-12">
                    <h1 class="text-center">Sign up</h1>
                    <p class="text-center">
                        <!-- <router-link to="{name: 'login'}">
                            Need an account?
                        </router-link> -->
                    </p>
                    VALIDATION ERRORS
                    <form>
                        <fieldset class="form-group">
                            <input class="form-control form-control-lg" 
                            type="text" 
                            placeholder="Username">
                        </fieldset>

                        <fieldset class="form-group">
                            <input class="form-control form-control-lg" 
                            type="text" 
                            placeholder="Email">
                        </fieldset>
                        
                        <fieldset class="form-group">
                            <input class="form-control form-control-lg" 
                            type="text" 
                            placeholder="Password">
                        </fieldset>
                    </form>
                </div>
                <div class="col-md-6 offset-md-3 col-xs-12 text-center">
                    <button class="btn btn-lg btn-primary">Sign up</button>
                    <button class="btn btn-lg btn-secondary" @click="increaseCount">Increase</button>
                    {{ count }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'McvRegister',
    computed: {
        count() {
            return this.$store.state.count;
        }
    },
    methods: {
        increaseCount(){
            this.$store.commit('increment');
        }
    }
}
</script>