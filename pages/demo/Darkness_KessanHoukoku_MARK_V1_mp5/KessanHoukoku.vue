<template>
    <div>
        <h1>決算報告書</h1>
        <table>
            <thead>
                <tr>
                    <th>項目</th>
                    <th>金額</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>売上高</td>
                    <td>100えん</td>
                </tr>
                <tr>
                    <td>経費</td>
                    <td>200えん</td>
                </tr>
                <tr>
                    <td>利益</td>
                    <td>100えん</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    async asyncData({ $axios }) {
        const response = await $axios.get('/api/kessan')
        return { kessanData: response.data }
    }
}
</script>