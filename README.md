# 基于业务需求改造一点东西的Element-ui,会不定期合并原始仓库

## 打包发布方式

执行 `npm run dist`
再改 package.json的版本号
然后 `npm publish`


# 更新说明

### select
增加一个`showDefaultLabel`属性,在默认value没有匹配到option时,默认显示空字符串,不显示其value

### tree
在元数据里增加一个customNodeClass属性,即可给node增加一个自定义样式

## LICENSE
[MIT](LICENSE)
