<template>
<div class="container">
  <div class="card">
    <div class="card-body">
      <h1>複合仕訳入力</h1>
      <div class="row">
        <div class="col-6">
          <div class="input-group mb-3">
            <span class="input-group-text"><h2>仕訳帳</h2></span>
            <div>
    <div>
      <label for="box1" :class="{ 'bright': box2Value !== '' }">Box 1:</label>
      <input type="text" id="box1" :class="{ 'bright': box2Value !== '' }" :disabled="true" />
    </div>
    <div>
      <label for="box2">Box 2:</label>
      <input type="text" id="box2" v-model="box2Value" />
    </div>
  </div>
            <thead>
              <tr>
                <th>年度<ReusableSelect :options="select1Options" :size="select1Size" /></th>
                <th>区分<ReusableSelect :options="select2Options" :size="select2Size" /></th>
                <th>会計単位<ReusableSelect :options="select3Options" :size="select3Size" /></th>
                <th>消費税<ReusableSelect :options="select4Options" :size="select4Size" /></th>
                <th>対象期間<ReusableSelect :options="select5Options" :size="select5Size" /></th>
              </tr>
            </thead>
          </div>
            <tbody>
              <tr>
                <span class="input-group-text"><td>科目</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>補助</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>名称</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>金額</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>消費税区分</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>消費税</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>部門</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
                <span class="input-group-text"><td>摘要</td></span>
                <input type="text" class="form-control" aria-label="jurnaNo">
              </tr>
            </tbody>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script setup >
import ReusableSelect from '~/components/ReusableSelect.vue';

useHead({
  title: 'My home page'
})

const select1Options = [
  { label: '2023', value: 'optionA' },
  { label: '2024', value: 'optionB' },
];
const select1Size = '70px';

const select2Options = [
  { label: '月次', value: 'optionA' },
  { label: '決算（中間）', value: 'optionB' },
  { label: '決算（期末）', value: 'optionC' },
  { label: '決算再振替', value: 'optionD' },
  { label: '期中', value: 'optionE' },
];
const select2Size = '115px';

const select3Options = [
  { label: '本社', value: 'optionE' },
];
const select3Size = '70px';

const select4Options = [
  { label: '原則課税/税抜処理', value: 'optionG' },
];
const select4Size = '170px';

const select5Options = [
  { label: '2023/1/1 ~ 2023/1/30', value: 'optionA' },
  { label: '2023/2/1 ~ 2023/2/28', value: 'optionB' },
  { label: '2023/3/1 ~ 2023/3/31', value: 'optionC' },
  { label: '2023/4/1 ~ 2023/4/30', value: 'optionD' },
  { label: '2023/5/1 ~ 2023/5/31', value: 'optionE' },
  { label: '2023/6/1 ~ 2023/6/30', value: 'optionF' },
  { label: '2023/7/1 ~ 2023/7/31', value: 'optionG' },
  { label: '2023/8/1 ~ 2023/8/31', value: 'optionH' },
  { label: '2023/9/1 ~ 2023/9/30', value: 'optionI' },
  { label: '2023/10/1 ~ 2023/10/31', value: 'optionJ' },
  { label: '2023/11/1 ~ 2023/11/30', value: 'optionK' },
  { label: '2023/12/1 ~ 2023/12/31', value: 'optionL' },
];
const select5Size = '200px';

</script>

<script>
export default {
  data() {
    return {
      box1Value: '科目',
      box2Value: '',
    };
  },
  watch: {
    box2Value(newVal) {
      // Box 2が変更されたら、Box 1が光るようにする
      if (newVal !== '') {
        this.makeBox1Bright();
      }
    },
  },
  methods: {
    makeBox1Bright() {
      // Box 1が光るようにするための処理（クラスを追加するなど）
      // 例: this.$refs.box1Label.classList.add('bright');
    },
  },
};
</script>

<style scoped>
.bright {
  background-color: #e6f7ff; /* 明るい色に変更する */
}
</style>