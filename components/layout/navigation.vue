<template>
    <section class="navigation">
        <div class="container">
            <!--<nuxt-link to="/" class="nav-logo" @click.native="closeNav">
                <logo-name></logo-name>
            </nuxt-link>-->

            <div class="mob-nav-btn" @click="navClick" :class="{ 'open-nav': showNav }">
                <div class="mob-nav-icon">
                    <div class="mob-nav-inner"></div>
                </div>
            </div>

            <div class="nav-block" :class="{ 'open-nav': showNav }">
                <ul>
                    <li><nuxt-link @click.native="closeNav" to="/" class="nav-btn">Home</nuxt-link></li>
                    <li><nuxt-link @click.native="closeNav" to="/about" class="nav-btn">About</nuxt-link></li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        head () {
            return {
                bodyAttrs: {
                    class: this.showNav ? 'nav-is-open' : ''
                }
            }
        },
        data () {
            return {
                showNav: false
            };
        },
        methods: {
            navClick: function () {
                this.showNav = !this.showNav;
            },
            closeNav: function () {
                this.showNav = false;
            }
        }
    }
</script>