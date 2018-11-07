https://blog.cloudboost.io/webpack-3-dynamic-imports-code-splitting-and-long-term-caching-made-easy-1892981e0ae7

new webpack.optimize.CommonsChunkPlugin({
    name: 'manifest'
}) 这里非常重要，否则更改某一个页面的话vendor.[hash].js又回重新打包，但这个包又是最大的，否则的话只有manifest这个包重新打，相比之下小多了。
