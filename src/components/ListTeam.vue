<template>
    <div>
        <router-link :to="{ name: 'listTeam' }" tag="button" class="btn btn-default glyphicon glyphicon-plus">List Team</router-link>
        <router-link :to="{ name: 'listPlayer' }" tag="button" class="btn btn-default glyphicon glyphicon-plus">List Player</router-link>
        <router-link :to="{ name: 'listManager' }" tag="button" class="btn btn-default glyphicon glyphicon-plus">List Manager</router-link>
        <router-link :to="{ name: 'HelloWorld' }" tag="button" class="btn btn-default glyphicon glyphicon-plus">Hello World</router-link>
        <hr/>
        <table class="table table-bordered">
            <thead>
                <tr>
                    <th>
                        ID
                    </th>
                    <th>
                        Team
                    </th>
                    <th>
                        City
                    </th>
                    <th>
                        Nation
                    </th>
                </tr>
            </thead>
            <tbody v-for="(item, index) in items">
                <tr>
                    <td>{{ index+1 }}</td>
                    <td>{{ item.team }}</td>
                    <td>{{ item.city }}</td>
                    <td>{{ item.nation }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
    export default {
        name : 'List',
        props: ['data'],
        data() {
            return {
                items: [
                    { 'team': 'Arsenal', 'city': 'London', 'nation': 'England' },
                    { 'team': 'Barcelona', 'city': 'Catalunya', 'nation': 'Spain' },
                    { 'team': 'Real Madrid', 'city': 'Madrid', 'nation': 'Spain' },
                    { 'team': 'Paris Saint Germain', 'city': 'Paris', 'nation': 'Franch' },
                    { 'team': 'Manchester City', 'city': 'Manchester', 'nation': 'England' },
                ]
            }
        }
    }
</script>
<style type="text/css">
    tr > th {
        text-align: center !important;
    }
</style>
