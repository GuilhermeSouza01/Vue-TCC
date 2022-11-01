<template>
    <div class="containerTable">
        <table>
            <thead>
                <tr class="table100-head">
                    <th className="column1">Indice</th>
                    <th className="column2">Nome</th>
                    <th className="column3">Idade</th>
                    <th className="column4">Número</th>
                    <th className="column5">Saldo</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in myData" :key="item">
                    <td>{{item.index + 1}}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.age}}</td>
                    <td>{{item.phone}}</td>
                    <td>{{item.balance}}</td>

                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>

import myData from "../db/json-tccfile.json";


let count = 1;
export default {
    name: "TableData",
    data() {
        return {
            myData,
            count,
        }
    }
}
</script>