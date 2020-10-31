<template>
  <div class="wrapper">
    <h2>iViewについて</h2>
    <div class="check">
      <h3>ボタン</h3>
      <Button type="primary">ボタン1</Button>
      <Button type="dashed">ボタン2</Button>
      <Button type="info">ボタン3</Button>
      <Button type="error">ボタン4</Button>
    </div>
    <div class="check">
      <h3>タグ</h3>
      <Tag>tag1</Tag>
      <Tag color="primary">tag2</Tag>
      <Tag type="border" closable color="success">tag3</Tag>
      <Tag type="dot" closable color="primary">tag4</Tag>
    </div>
    <div class="check">
      <h3>スター</h3>
      <Rate show-text v-model="valueText" />
    </div>
    <div class="check">
      <Menu mode="horizontal" :theme="theme1" active-name="1">
        <MenuItem name="1">
          <Icon type="ios-paper" />
          内容管理
        </MenuItem>
        <MenuItem name="2">
          <Icon type="ios-people" />
          用户管理
        </MenuItem>
        <Submenu name="3">
          <template slot="title">
            <Icon type="ios-stats" />
            统计分析
          </template>
          <MenuGroup title="使用">
            <MenuItem name="3-1">新增和启动</MenuItem>
            <MenuItem name="3-2">活跃分析</MenuItem>
            <MenuItem name="3-3">时段分析</MenuItem>
          </MenuGroup>
          <MenuGroup title="留存">
            <MenuItem name="3-4">用户留存</MenuItem>
            <MenuItem name="3-5">流失用户</MenuItem>
          </MenuGroup>
        </Submenu>
        <MenuItem name="4">
          <Icon type="ios-construct" />
          综合设置
        </MenuItem>
      </Menu>
    </div>

    <div class="check">
      <h3>メッセージ</h3>
      <Button type="primary" @click="info">メッセージ表示</Button>
    </div>

    <div class="check">
      <h3>ステップ</h3>
      <Steps :current="1">
        <Step title="ステップ1" content="内容1"></Step>
        <Step title="ステップ2" content="内容2"></Step>
        <Step title="ステップ3" content="内容3"></Step>
        <Step title="ステップ4" content="内容4"></Step>
      </Steps>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped lang="scss">
.wrapper {
  margin-top: 100px;
  .check {
    margin-top: 20px;
  }
  .kekka {
    font-size: 30px;
  }
}
</style>
