<template>
    <div>
        <div class="galleria">
            <div class="galleria-item">
                <div class="galleria-content">
                    <h3>01</h3>
                    <h2>The best flower shop <br> in Moscow!</h2>
                    <div class="galleria-line"></div>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et</p>
                </div>
                <button>View catalog</button>
            </div>
        </div>

        <div class="reasons">
            <h2>Why FlowerStore?</h2>
            <div class="row1">
                <div class="reason-small" id="delivery">
                    <h3 class="reason-header">Fast delivery</h3>
                    <p class="reason-subheader">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                    <img src="../static/Delivery.png" alt="delivery_man">
                </div>
                <div class="reason-big" id="fresh">
                    <h3 class="reason-header">Always fresh flowers</h3>
                </div>
            </div>
            <div class="row2">
                <div class="reason-big" id="types">
                    <h3 class="reason-header">200+ types of flowers</h3>
                </div>
                <div class="reason-small" id="clock">
                    <h3 class="reason-header">Everyday, 24h</h3>
                    <p class="reason-subheader">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
                    <img src="../static/clock.png" alt="clock">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            images: ['../src/static/banner/1.jpg',
            '../src/static/banner/2.jpg',
            '../src/static/banner/3.jpg'],
        };
    },
};
</script>

<style scoped>
.row1{
    display: grid;
    grid-template-columns: 1fr 2fr;

    grid-template-rows: 20vw;

    grid-column-gap: 30px;
}
.row2{
    margin-top: 30px;
    display: grid;
    grid-template-columns: 2fr 1fr;

    grid-template-rows: 20vw;

    grid-column-gap: 30px;
}

.reason-small, .reason-big{
    background-color: #F4F4F4;
    height: 100%;
    width: 100%;
    position: relative;
    cursor: help;
}

.reasons{
    margin-top: 80px;
    padding: 0 500px;
}

#delivery{
    background: rgb(240,210,209);
    background: linear-gradient(131deg, rgba(240,210,209,1) 0%, rgba(246,239,166,1) 100%);
}

.reason-header{
    font-size: 2rem;
    margin: 30px 0 0 30px;
}

.reason-subheader{
    font-size: 1.5rem;
    margin: 15px 0 0 30px;

    opacity: 0;
    transition: all .2s ease;
}

.reason-small img{
    position: absolute;
    right: 0;
    bottom: 0;
    width: 80%;
    transition: width .2s ease;
}

#delivery:hover img{
    width: 90%;
}

#delivery:hover p{
    opacity: 1;
}

#clock{
    background: rgb(240,210,209);
    background: linear-gradient(311deg, rgba(240,210,209,1) 0%, rgba(246,239,166,1) 100%);
}

#clock img{
    width: 60%;
}

#clock:hover img{
    width: 70%;
}

#clock:hover p{
    opacity: 1;
}

#fresh{
    background-image: url('../static/fon1.jpg');
    background-repeat: no-repeat;
    background-size: 100%;
    object-fit: cover;

    transition: all .2s ease;
}

#types{
    background-image: url('../static/fon2.jpg');
    background-repeat: no-repeat;
    background-size: 100%;
    object-fit: cover;

    transition: all .2s ease;
}

#types .reason-header{
    color: #515f58;
}

#fresh .reason-header{
    color: #515f58;
}

#fresh:hover, #types:hover{
    background-size: 110%;
}


.galleria{
    width: 100%;
    padding: 0 500px;
    height: 700px;

    background-image: url('../static/1699277741_binomen-ru-p-serii-fon-s-zelenyu-pinterest-15.jpg');
    background-size: 100%;
}


.galleria-content h3, h2{
    font-size: 3rem;
    margin: 0;
}

.galleria-content h2{
    color: #1D2029;
}

.galleria-content h3{
    color: #8EB19D;
}
.galleria-line{
    height: 5px;
    width: 100px;
    background-color: #8EB19D;
}

.galleria-item button{
    background-color: #8EB19D;
    border-radius: 5px;
    width: 200px;
    height: 40px;
    font-family: 'Montserrat';
    border: none;
    color: white;
    transition: all .2s ease;
    
    margin-top: 50px;
}

.galleria-item button:hover{
    background-color: #769282;
    cursor: pointer;
}

.galleria-item{
    display: flex;
    flex-direction: column;
    height: 100%;
    justify-content: center;
}
</style>