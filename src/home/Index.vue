<template>
  <KView class="page form js_show">
    <KView class="page__hd">
      <h1 class="page__title">Form</h1>
      <p class="page__desc">form 表单内容</p>
    </KView>
    <KCells
      checkbox
      title="Checkbox">
      <KCheckboxGroup
        v-model="checkboxGrpValues"
        @change="handleChange">
        <KCheckbox value="零度的田">零度的田</KCheckbox>
        <KCheckbox value="小程序开发">小程序开发</KCheckbox>
      </KCheckboxGroup>
    </KCells>
    <KCells title="Switch">
      <KSwitch
        v-model="switchItem"
        label="Switch文本" />
    </KCells>

    <KCells title="健康信息登记表">
      <KInput
        v-model="inputUserName"
        label="姓名"
        placeholder="填写本人姓名"
        clearable
        @change="inputChange"/>
      <KRadioGroup
        v-model="genderValue"
        @change="genderChange">
        <KRadio :value="male">男</KRadio>
        <KRadio :value="female">女</KRadio>
      </KRadioGroup>
      <KInput
        v-model="inputNickName"
        label="昵称"
        placeholder="填写本人微信号的昵称"
        clearable
        @change="inputChange"/>
    </KCells>


  </KView>
</template>

<script>
export default {
  data() {
    return {
      singleCheckbox: false,
      checkboxGrpValues: [],
      inputCardValue: '',
      inputNickName: '',
      switchItem: false,
      radioValue: 1
    }
  },
  methods: {
    handleChange() {
      console.log(this.checkboxGrpValues)
    },
    singleCheckboxHandler() {
      console.log(this.singleCheckbox)
    },
    raidoChange() {
      console.log(this.radioValue)
    },
    inputChange() {
      console.log(this.inputValue)
    }
  }
}
</script>
