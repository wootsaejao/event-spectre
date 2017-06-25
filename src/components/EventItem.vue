<template lang="html">
    <div class="box">
        <article class="media">
            <div class="media-left">
                <figure class="image is-64x64">
                    <img :src="picture" :alt="title" />
                </figure>
            </div>
            <div class="media-content">
                <div class="content">
                    <p>
                        <a :href="url" target="_blank" rel="noopener"><strong>{{ title }}</strong></a><br />
                        <small>start: {{ datetime }}</small>
                    </p>
                </div>
            </div>
        </article>
    </div>
</template>

<script>
import moment from 'moment-timezone'
export default {
    props: {
        picture: {
            type: String,
            default: 'http://localhost:4000/images/placeholders/128x128.png'
        },
        title: {
            type: String,
            default: 'Title Naja'
        },
        datetimeIso: {
            type: String,
            default: '2017-08-03T05:04:05+07:00',
        },
        url: {
            type: String,
            default: 'http://google.com'
        }
    },
    computed: {
        datetime () {
            return moment(this.datetimeIso).fromNow()
        }
    }
}
</script>

<style scoped lang="scss">
.image img {
    position: absolute;
    top: 0; bottom:0; left: 0; right:0;
    margin: auto;
}
</style>
