### This is a tool to convert px to vh vw


This is a tool to convert px to vh vw based on media query results,

Usually px will be converted to vh, if the screen ratio is 16/9, px will be converted to vw

The purpose of this is to try to keep the page as original as possible when the screen ratio changes. 

#### install:

```
npm i @ha/px2vwh-loader
```

or

```
yarn add @ha/px2vwh-loader
```

#### config:
webpack:
```
module: {
  rules: [{
    test: /\.(sc|sa)ss$/,
    loader:'@ha/px2vwh-loader',
      query:{
        uiHeight:737,
        uiWidth:1283,
        decimal:3
      }
  }]
}

```
webpack-chain:

```
config.module
      .rule('px2vwh')
      .test( /\.(sc|sa)ss$/)
      .use('@ha/px2vwh-loader')
      .loader('@ha/px2vwh-loader')
      .options({
        uiHeight:737,
        uiWidth:1283,
        decimal:3
      })
      .end()
```
