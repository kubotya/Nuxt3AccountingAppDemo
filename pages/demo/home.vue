<template>
  <Container>
    <div class="row">
      <div class="col">
        <div class="card">
          <div class="card-header">各種入力</div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item"><NuxtLink to="/demo/complex-journal/complex" class="card-link">複合仕訳入力</NuxtLink></li>
            <li class="list-group-item"><NuxtLink to="/demo/passbook/passbook" class="card-link">通帳入力</NuxtLink></li>
        </ul>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <div class="card-header">各種出力</div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item"><NuxtLink to="/demo/bookKeepingJournal/journalbook" class="card-link">仕訳帳</NuxtLink></li>
            <li class="list-group-item"><NuxtLink to="/demo/journaList_Search/search" class="card-link">仕訳検索</NuxtLink></li>
            <li class="list-group-item">
              <NuxtLink to="/accountledger" class="card-link">総勘定元帳</NuxtLink>
            </li>
            <li class="list-group-item"><NuxtLink to="/demo/hojomototyou/subledger" class="card-link">補助元帳</NuxtLink></li>
          </ul>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <div class="card-header">年次決算</div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item"><NuxtLink to="/demo/Darkness_KessanHoukoku_MARK_V1_mp5/KessanHoukoku" class="card-link">決算報告書</NuxtLink></li>
          </ul>
        </div>
      </div>
      <div class="col">
        <div class="card">
          <div class="card-header">各種設定</div>
          <ul class="list-group list-group-flush">
            <li class="list-group-item">
              <NuxtLink to="/accountinginfoconfig" class="card-link">会社基本設定</NuxtLink>
            </li>
            <li class="list-group-item">
              <NuxtLink to="/demo/BasicInformationSetting/AccountItem" class="card-link">勘定科目</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </Container>
</template>
