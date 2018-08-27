<template>
    <div class="footer">
        <div v-for='(item for items)' :class='[item.cls,{on:index === idx}]' @click="$router.push(item.push)">
            <img :src='index === idx?item.iconSelect:item.icon' >
            <p :class="['colorChange',{on:index===idx}]">{{item.name}}</p>
        </div>
    </div>
</template>
<script>
    export default {
        props:['idx'],
        data:()[
            return {
                items:[{
                    cls:"home",
                    name:"首页",
                    push:"/home",
                    icon:"../static/home.png",
                    iconSelect:"../static/home_select.png"
                },
                {
                    cls:"shares",
                    name:"股票",
                    push:"/shares",
                    icon:"../static/shares.png",
                    iconSelect:"../static/shares_select.png"
                },{
                    cls:"community",
                    name:"社区",
                    push:"/community",
                    icon:"../static/community.png",
                    iconSelect:"../static/community_select.png"
                },{
                    cls:"mine",
                    name:"我的",
                    push:"/mine",
                    icon:"../static/mine.png",
                    iconSelect:"../static/mine_select.png"
                }]
            }
        ]
    }
</script>

