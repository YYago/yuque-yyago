# yuque-yyago

语雀API。

1. 用 [request-promise](https://www.npmjs.com/package/request-promise) 实现——*其实是没有必要的，只是我在其他项目上用，顺便分出来做一个 package。一次性的项目可以直接用 `request-promise` 这类包。*
2. 函数命名可能与官方不一致，具体见[Doc](https://yyago.github.io/yuque-yyago/)。
5. 部分参数虽注释有默认值，但并没有赋值，使用的时候可能还是要赋值。
6. 无附件(图片)上传功能（OAUTH应用才有权限）。

> 操作权限取决于 Token 权限以及用户在团队、知识库中的权限。

## Example

```js
const yuque = require('yuque-yyago');
const api = new yuque('你的Token'); 

// creat a group.
api.group_create('语雀 API for Nodejs','yuqueAPI-for-Nodejs','语雀API Nodejs 版').then(res=>{
        console.log(`${JSON.stringify(res)}`)
    }).catch(e=>{
        console.log(e)
})
```