<template>
    <div class="container">
    <header class="d-flex justify-content-center py-3">
      <ul class="nav nav-pills">
        <li class="nav-item"><a v-bind:href="routeNamesArray[0].path" class="nav-link active" aria-current="page">{{ routeNamesArray[0].name }}</a></li>
        <li class="nav-item"><a v-bind:href="routeNamesArray[1].path" class="nav-link active" aria-current="page">{{ routeNamesArray[1].name }}</a></li>
        <li class="nav-item"><a href="#" class="nav-link">Pricing</a></li>
        <li class="nav-item"><a href="#" class="nav-link">FAQs</a></li>
        <li class="nav-item"><a href="#" class="nav-link">About</a></li>
      </ul>
    </header>
  </div>
</template>


<script>
    import router from '@/router'
    export default {
        name: 'ThisIsExample',
        props: {
            msg: String
        },
        data() {
            return {
                router,
                routeNamesArray: []
            }
        },
        created(){
            this.routeNames()
        },
        methods: {
            routeNames () {
                const aux = []
                this.router.getRoutes().forEach(element => aux.push( 
                    {
                        name: element.name, 
                        path: element.path
                    } 
                ));
                this.routeNamesArray = aux;
                console.log(aux);
                return aux
            }
        }
    }
</script>