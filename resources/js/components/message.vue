<template>
<div>
         <li class="list-group-item" :class="className"><slot></slot> </li>
        <small class="badge float-right " :class="classbadge">You</small>

</div>
</template>

<script>
    export default {
        props:[
            'color',
        ],

        computed: {
            className(){
                console.log('list-group-item-'+this.color);
                return 'list-group-item-'+this.color;
            },
            classbadge(){
                 return 'badge-'+this.color;

            }
        },

        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
