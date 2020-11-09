<template>
    <div id="app">
        <h1 class="header">Movie Night</h1>
        <div id="menu">
            <div id="brand">

            </div>
            <div id="side">
                <router-link to="/">
                    <div class="menu-item browse">
                        <p>Home</p>
                    </div>
                </router-link>
                <router-link to="/browse">
                    <div class="menu-item browse">
                        <p>Filter</p>
                    </div>
                </router-link>
                <router-link to="/cart">
                    <div class="menu-item">
                        <p>About</p>
                    </div>
                </router-link>
            </div>
        </div>
        <router-view />
        <a class="footer" href="https://github.com/KalidinStorm/cs260cp3.git">https://github.com/KalidinStorm/cs260cp3.git</a>
    </div>
    
</template>


<style>
    p {
        padding: 5px 20px;
    }

    .header {
        font-family: "kufam";
        background-color: lightgrey;
        font-size: 50px;
        padding: 50px;
        text-align: center;
        padding-left: 10px;
        padding-right: 10px;
        border: 1px solid #5D6063;
        border-radius: 20px;
        font-weight: normal;
    }

    .footer {
        display: flex;
        justify-content: center;
        align-items: center;
        color: #FFF;
        background: lightgrey;
        font-weight: bold;
        padding: 10px;
        margin: 10px 0;
        border: 2px solid #5D6063;
        border-radius: 20px;
        height: 200px;
        width: auto;
    }

    * {
        box-sizing: border-box;
    }

    body {
        margin: 50px 100px;
    }

    #menu {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-column-gap: 5px;
        grid-template-areas: "none brand side";
        margin-bottom: 50px;
    }

        #menu a {
            color: black;
            
        }

    #brand {
        grid-area: brand;
        display: flex;
        justify-content: center;
    }

        #brand img {
            height: 200px;
        }

    #side {
        grid-area: side;
        display: flex;
        justify-content: flex-end;
    }

        #side img {
            width: 50px;
        }

    .menu-item {
        display: flex;
        flex-direction: column;
        background-color: #bebebe;
        border: 1px solid #5D6063;
        border-radius: 5px;
    }

        .menu-item p {
            margin: 0px;
        }

    .browse {
        margin-right: 50px;
    }

    
</style>
