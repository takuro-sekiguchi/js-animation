# animation

[作成したサイト](https://taku-web3.com/project/js-animation/index.html)

## ■今回新しく学んだこと
- JavaScript animation engineの使い方



### JavaScript animation engine
[公式サイト](https://animejs.com/)

[ドキュメント](https://animejs.com/documentation/)
基本的にはドキュメントを見て使い方を覚える


```js

function test() {
  anime({
    target: '.target',
    duration: 1000,
    delay: anime.stagger(10),
    //アニメーションが終了したら繰り返す処理
    complete: test,
    translateX: function() {
      return anime.random(-700, 800);
    },
    translateY: function() {
      return anime.random(-500, 500);
    },
    scale: function() {
      return anime.random(1, 3);
    },
    //使用可能なメソッドはドキュメントを参考にする
  })
}

```


div要素を50個作る方法(for文でループ処理する)
```js
for(let i = 0; i <= 50; i++){
  //div要素を生成する
  const blocks = document.createElement('div');
  //div要素にblockというクラス名をつける
  blocks.classList.add('block');
  //containerの子要素としてblockを追加する。
  container.appendChild(blocks);
}
```