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
                        Name
                    </th>
                    <th>
                        Team
                    </th>
                    <th>
                        Nation
                    </th>
                </tr>
            </thead>
            <tbody v-for="(item, index) in items">
                <tr>
                    <td>{{ index+1 }}</td>
                    <td>{{ item.name }}</td>
                    <td>{{ item.team }}</td>
                    <td>{{ item.nation }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
<script>
    export default {
        name : 'List',
        data() {
            return {
                items: [
                    { 'name': 'Pep Guardiola', 'team': 'Manchester City', 'nation': 'Spain' },
                    { 'name': 'Arsene Wenger', 'team': 'Arsenal', 'nation': 'France' },
                    { 'name': 'Le Thuy Hai', 'team': 'Becamex Binh Duong', 'nation': 'Viet Nam' },
                    { 'name': 'Park Han Seo', 'team': 'Viet Nam', 'nation': 'Korea' },
                    { 'name': 'Jose Mourinho', 'team': 'Manchester United', 'nation': 'Portugal' },
                    { 'name': 'Carlo Ancelotti', 'team': 'Bayern Munich', 'nation': 'Italia' },
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
