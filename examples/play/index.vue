<template>
  <div style="margin: 20px;">
    <el-tree ref="tree" :data="data" node-key="id" :show-checkbox="true">
      <span class="custom-tree-node" slot-scope="{ node, data }">
        <span class="auth-name">{{ data.label }}</span>
      </span>
    </el-tree>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          label: '一级 2',
          children: [
            {
              id: 3,
              label: '二级 2-1',
              children: [
                {
                  id: 4,
                  label: '三级 3-1-1',
                  customNodeClass: 'qwertyui',
                },
                {
                  id: 5,
                  label: '三级 3-1-2',
                  customNodeClass: 'qwertyui',
                }
              ]
            },
            {
              id: 2,
              label: '二级 2-2',
              disabled: true,
              children: [
                {
                  id: 6,
                  label: '三级 3-2-1'
                },
                {
                  id: 7,
                  label: '三级 3-2-2',
                  disabled: true
                }
              ]
            }
          ]
        }
      ],
      input: 'Hello Element UI!',
      value: '',
      options: [
        {
          value: 1,
          label: '一'
        },
        {
          value: 2,
          label: '二'
        }
      ]
    };
  }
};
</script>


<style>
  .qwertyui {
    border: 1px solid;
  }
</style>