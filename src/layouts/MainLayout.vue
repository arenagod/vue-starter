<template>
<div>
    <Header/>
    <section>
    <router-view/>
    </section>
    <Footer/>
</div>
</template>

<script>
import Header from './Header';
import Footer from './Footer';

export default {
    components: {
        Header, Footer
    }
}
</script>