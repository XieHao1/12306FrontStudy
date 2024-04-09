<template>
  <Space direction="vertical" :style="{ width: '100%' }">
    <Card title="乘客信息（填写说明）">
      <div>
        <Space>
          <UserOutlined />
          乘车人
        </Space>
      </div>
      <dvi>
        <Space>
          <Checkbox>旺旺</Checkbox>
          <Checkbox>小伙</Checkbox>
        </Space>
      </dvi>
      <Divider dashed></Divider>
      <Form></Form>
      <Table :columns="columns" :data-source="dataSource"></Table>
    </Card>
  </Space>
</template>

<script setup>
import {
  Card,
  Space,
  Divider,
  Checkbox,
  Table,
  Form,
  FormItem
} from 'ant-design-vue'
import { UserOutlined } from '@ant-design/icons-vue'

const columns = [
  {
    dataIndex: 'number',
    title: '序号'
  },
  {
    dataIndex: 'ticket',
    title: '票种'
  },
  {
    dataIndex: 'seat',
    title: '席别'
  },
  {
    dataIndex: 'name',
    title: '姓名'
  },
  {
    dataIndex: 'cardType',
    title: '证件类型'
  },
  {
    dataIndex: 'cardNumber',
    title: '证件号码'
  },
  {
    dataIndex: 'eidt',
    title: '操作'
  }
]

const dataSource = [
  {
    number: 1,
    ticket: '成人票',
    seat: '二等座',
    name: 'yika',
    cardType: '证件类型',
    cardNumber: '证件号码',
    eidt: '操作'
  },
  {
    number: 1,
    ticket: '成人票',
    seat: '二等座',
    name: 'yika',
    cardType: '证件类型',
    cardNumber: '证件号码',
    eidt: '操作'
  },
  {
    number: 1,
    ticket: '成人票',
    seat: '二等座',
    name: 'yika',
    cardType: '证件类型',
    cardNumber: '证件号码',
    eidt: '操作'
  }
]
</script>

<style lang="scss" scoped>
.train-title {
  display: flex;
}
</style>
