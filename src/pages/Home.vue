<template>
    <main>
        <div class="text-top">Vídeos novos toda <b>quinta</b> as <b>20h</b></div>
        <a href="https://youtube.com/wdevoficial" target="blank"><img src="https://raw.githubusercontent.com/william-costa/wdev-mock-site-resources/master/assets/images/subscribe.svg
" alt="Inscreva-se" id="subscribe"></a>
        <div class="text-bottom">youtube.com/wdevoficial</div>
    </main>
</template>

<script>
export default {
    name: 'homE',
    
}
</script>

<style scoped>

main{
    background-color: var(--color-background-home);
    justify-content: center;
    align-items: center;
}

.text-top{
    color: var(--color-text-light);
    font-size: 22px;
    margin-bottom: 20px;
}

.text-bottom{
    color: var(--color-text-light);
    font-size: 18px;
    margin-bottom: 20px;
}

#subcribe{
    width: 340px;
}

@media (min-width:700px){
    #subcribe{
        width: 370px;
    }
}

</style>