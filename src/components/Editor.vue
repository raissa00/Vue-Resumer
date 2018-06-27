<template>
    <div id="editor">
        <nav>
            <ol>
                <li v-for="i in [0, 1, 2, 3, 4, 5]" 
                    v-bind:class="{active: currentTab === i}"
                    v-on:click="currentTab = i"
                    >
                    <svg class="icon" aria-hidden="true">
                        <use v-bind:xlink:href="`#icon-${icons[i]}`"></use>
                    </svg>
                </li>
            </ol>
        </nav>
        <ol class="panel">
            <li v-for="i in [0, 1, 2, 3, 4, 5]" 
                v-bind:class="{active: currentTab === i}"
            >
                <div v-html="`${i}`"></div>
            </li>
        </ol>
    </div>
</template>

<script>
export default {
    data() {
        return {
            currentTab: 0,
            icons: ['card', 'work', 'book', 'projects', 'trophy', 'phone']
        }
    }
}
</script>


<style lang="scss">
    #editor {
        display: flex;
        > nav {
            background: #000;
            width: 80px;
            
            > ol > li {
                padding: 8px 0;
                text-align: center;
                > .icon {
                    width: 24px;
                    height: 24px;
                    fill: white;
                }
                &.active {
                    background: #fff;
                    > .icon {
                        fill: #000;
                    }
                }
            }
            
        }
        > .panel {
            > li {
                display: none;
                &.active {
                    display: block;
                }
            }        
        }
    }
    
</style>
