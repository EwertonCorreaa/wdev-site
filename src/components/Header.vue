<template>
    <header>
        <nav class="container">
            <a href="/"><img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
" id="logo" alt="WDEV"></a>

            <img v-on:click="openMenu" src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/menu.svg" id="menu-button" alt="Abrir menu">

            <div v-on:click="closeMenu" id="menu-overlay" v-if="menuActive"></div>

            <div id="menu-itens" :class="{active:menuActive}">
                <a href="/"><img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/wdev.svg
" id="menu-logo" alt="WDEV"></a>

                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/">Video</a></li>
                    <li><a href="/">Sobre</a></li>
                    <li><a href="/">Contato</a></li>
                </ul>
            </div>
        </nav>

    </header>
</template>

<script>
export default {
    name: 'headeR',
    data() {
        return {
            menuActive: false

        }
    },
    methods:{
        openMenu: function(){
            this.menuActive = true;
        },
        closeMenu: function(){
            this.menuActive = false;
        }
    }
}
</script>

<style scoped>
header{
    background-color: var(--color-background-nav);
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: center; 
    align-items: center;
}

nav{
    display: flex;
    justify-content: space-between;
    height: 60px;
    align-items: center;
}

#logo{
    width: 130px;
}

#menu-button{
    width: 30px;
}

#menu-overlay{
    position: fixed;
    top: 0;
    left: 0;
    width: 40%;
    height: 100vh;
    background-color: black;
    opacity: 0.8;
}

#menu-logo{
    width: 110px;
    margin-top: 30px;
    margin-bottom: 10px;

}

#menu-itens{
    position: fixed;
    top: 0;
    right: 0;
    background-color: var(--color-background-nav);
    width: 60%;
    height: 100vh;
    display: none;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
}

#menu-itens.active{
    display: flex;
}

ul{
    list-style: none;
    text-align: center;
}

ul li{
    margin: 20px 0px;
    
}

ul li a{
    color: var(--color-text-light);
}

@media (min-width: 700px) {
    #menu-button,
    #menu-logo,
    #menu-overlay{
        display: none;
    }

    #menu-itens{
        display: flex;
        position: static;
        height: 60px;
        width: auto;
    }

    ul{
        display: flex;
        height: 60px;
        align-items: center;
    }

    ul li{
        margin: 0;
        margin-left: 20px;
    }
}



</style>



