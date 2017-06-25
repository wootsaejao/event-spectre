<template lang="html">
    <div>
        <div class="section">
            <div class="container">
                <h1 class="title">Event Spectre</h1>
                <h2 class="subtitle">Never miss awesome events</h2>
                <event-item v-for="item in events" :key="item.id" :title="item.title" :picture="item.picture" :datetimeIso="item.datetimeIso" :url="item.url" />
            </div>
        </div>
    </div>
</template>

<script>
import EventItem from '@/components/EventItem'
export default {
    components: {
        'event-item': EventItem,
    },
    data () {
        return {
            events: [
                {
                    id: 1,
                    title: 'PWA Online Hackathon',
                    picture: 'https://raw.githubusercontent.com/bkkjs/pwa-online-hackathon/master/public/Icon-196.png',
                    datetimeIso: '2017-06-23T20:00:00+07:00',
                    url: 'https://pwa.online.hackathon.in.th',
                },
                {
                    id: 2,
                    title: 'Startup Thailand 2017 Bangkok',
                    picture: 'https://scontent.fbkk12-2.fna.fbcdn.net/v/t1.0-9/14729397_1362650690411931_38082616714980259_n.png?oh=3dae5106a293610b5f98923da7b61df6&oe=59D010DC',
                    datetimeIso: '2017-07-06T10:00:00+07:00',
                    url: 'https://www.facebook.com/events/1940523022890697',
                },
                {
                    id: 3,
                    title: 'TECHJAM 2017',
                    picture: 'https://www.blognone.com/sites/default/files/styles/thumbnail/public/news-thumbnails/techjam.jpg',
                    datetimeIso: '2017-07-28T09:00:00+07:00',
                    url: 'http://www.techjam.tech/',
                }
            ]
        }
    }
}
</script>

<style lang="css">
</style>
