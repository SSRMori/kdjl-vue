<template>
    <div class="map">
        <div class="title-logo"></div>
        <div class="next">
            <router-link to="/twoCity"></router-link>
        </div>
        <div class="exchange">
            <router-link to="/exchange"></router-link>
        </div>
        <div class="pasture">
            <router-link to="/pasture"></router-link>
        </div>
        <div class="mystery">
            <router-link to="/mysteryShop"></router-link>
        </div>
        <div class="warehouse">
            <router-link to="/warehouse"></router-link>
        </div>
        <div class="prop">
            <router-link to="/propShop"></router-link>
        </div>
        <div class="smithy">
            <router-link to="/propShop"></router-link>
        </div>
        <div @click="exchange" class="palace">
            <router-link to="/propShop"></router-link>
        </div>
        <div @click="exchange" class="notice">
            <router-link to="/propShop"></router-link>
        </div>
    </div>
</template>

<script>
    export default {
        name: "CenterCity",
        methods: {
            exchange: function () {
                alert('暂未开放，敬请期待！')
            }
        }
    }
</script>

<style scoped lang="scss">
    .title-logo {
        background: url("../../../public/images/cities/map_logo_new.png") no-repeat;
        width: 788px;
        height: 311px;
        /*z-index: 10;*/
    }

    a {
        display: inline-block;
    }

    .map {
        background: url("../../../public/images/cities/map.png") no-repeat;
        width: 789px;
        height: 312px;
        > *:not(.title-logo) {
            position: absolute;
            cursor: pointer;
        }
        .next {
            background: url("../../../public/images/cities/next.png") no-repeat;
            top: 125px;
            right: 0;
            z-index: 10;
            animation: next 400ms linear infinite alternate;
            > a {
                width: 59px;
                height: 41px;
            }
        }

        @keyframes next {
            from {right: 0;}
            to {right: 20px;}
        }

        .exchange {
            bottom: 7px;
            left: 11px;
            > a {
                width: 202px;
                height: 154px;
            }
            &:hover {
                background: url('../../../public/images/cities/1.png') no-repeat;
            }
        }

        .pasture {
            top: 0;
            left: 0;
            width: 110px;
            height: 74px;
            > a {
                width: 110px;
                height: 74px;
            }
            &:hover {
                background: url('../../../public/images/cities/2.png') no-repeat;
            }
        }

        .mystery {
            top: 20px;
            left: 183px;
            > a {
                width: 221px;
                height: 200px;
            }
            &:hover {
                background: url('../../../public/images/cities/3.png') no-repeat;
            }
        }

        .warehouse {
            top: 0;
            right: 312px;
            > a {
                width: 150px;
                height: 141px;
            }
            &:hover {
                background: url('../../../public/images/cities/4.png') no-repeat;
            }
        }

        .prop {
            right: 123px;
            top: 0;
            > a {
                width: 190px;
                height: 137px;
            }
            &:hover {
                background: url('../../../public/images/cities/5.png') no-repeat;
            }
        }

        .smithy {
            right: 0;
            top: 0;
            > a {
                width: 142px;
                height: 162px;
            }
            &:hover {
                background: url('../../../public/images/cities/6.png') no-repeat;
            }
        }

        .palace {
            right: 0;
            bottom: 19px;
            > a {
                width: 286px;
                height: 178px;
            }
            &:hover {
                background: url('../../../public/images/cities/7.png') no-repeat;
            }
        }

        .notice {
            bottom: 80px;
            right: 270px;
            > a {
                width: 61px;
                height: 87px;
            }
            &:hover {
                background: url('../../../public/images/cities/8.png') no-repeat;
            }
        }
    }
</style>