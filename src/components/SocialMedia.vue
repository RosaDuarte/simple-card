<template>
    <div class="social-media">
        <span class="img"></span>
        <div>
            <span>
                <a href="https://twitter.com/rosaelissa" target="a_black"><i class="fa-brands fa-twitter"></i></a>
            </span>
            <span>
                <a href="https://www.instagram.com/rosa_elissa/" target="a_black"><i class="fa-brands fa-instagram"></i></a>
            </span>
            <span>
                <a href="https://www.facebook.com/RosaElisaD/" target="a_black"><i class="fa-brands fa-facebook"></i></a>   
            </span>
            <span>
                <a href="https://www.linkedin.com/in/rosa-duarte-/" target="a_black"><i class="fa-brands fa-linkedin"></i></a>     
            </span>
            <span>
                <a href="https://github.com/RosaDuarte" target="a_black"><i class="fa-brands fa-github"></i></a>  
            </span>
        </div>
    </div>   
</template>

<script>
export default{
    props: ['mode']
}
</script>


<style scoped>
    .dark .social-media div span i{
        color: var(--sand);
    }
    .social-media{
        position: relative;
    }
    .img{
        background-image: url("../assets/image/flowers.png");
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        width: 80px;
        height: 80px;
        position: absolute;
        transform: rotate(45deg);
        top: -45px;
        left: calc(50% - 35px);
        
    }
    .social-media div{
        height: 50px;
        margin: 15px 0 0;
        position: relative;
    }
    .social-media div span{
        margin: 5px 5px 0;
    }
    .social-media div span i{
        font-size: 40px;
        color: var(--light-green);
    }
    .social-media div span i:hover{
        font-size: 40px;
        color: var(--old-pink);
        transform: rotate(20deg);
    }
</style>