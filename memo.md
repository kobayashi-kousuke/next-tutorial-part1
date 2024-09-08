# NextJs Tutorial

## スプレッド構文  
```
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2); // [1, 2, 3, 4, 5]
```
配列やオブジェクトを展開して、その要素やプロパティをコピーしたり、他の配列やオブジェクトに渡したりするために使用する。  

## レスト構文  
```
const [first, ...rest] = [1, 2, 3, 4];
console.log(first); // 1
console.log(rest); // [2, 3, 4]
```
関数の引数や配列・オブジェクトの残りの要素を1つの変数にまとめるために使用する。  

## 同期処理と非同期処理  
* 同期処理（sync）  
通常のコードで、順番に処理をしていく処理
* 非同期処理（async）  
非同期処理はコードを順番に処理していくが、ひとつの非同期処理が終わるのを待たずに次の処理を評価する。 つまり、非同期処理では同時に実行している処理が複数ある。  

## ソート
```
PostsData.sort((a, b) => {
  if (a.date < b.date) {
    return 1;
  } else {
    return -1;
  }
});
```
PostsDataをdateでソートする構文。  
a.date < b.date の場合、return 1 としているので、aをbの後ろに配置  
a.date >= b.date の場合は return -1 として、aをbの前に配置  

## 名前付きエクスポート（named export）
```
export const sampleFn = () => {
  return <h1>サンプル</h1>
}
```
* 呼び出し方  
```
import {sampleFn} from './Sample'
```
* 特徴  
１つのモジュール内に複数exportできる  
呼び出し側では、export時の名前でimportしなければならない

## デフォルトエクスポート（default exports）
```
const sampleFn = () => {
  return <h1>サンプル</h1>
}
export default sampleFn
```
* 呼び出し方  
```
import sampleFn from './Sample'
```
* 特徴  
１つのモジュール内に1つだけexportできる  
呼び出し側で、名前を自由に定義できる

## NextJsフォルダ構成イメージ
src/  
├── components/　・・・　様々なコンポーネントをまとめたフォルダ  
│   ├── base/　・・・　サイト全体を構成するコンポーネント（ヘッダー、レイアウト系、metaタグなど）  
│   ├── page/　・・・　pages/の中身の実態があるフォルダ  
│   └── ui/　・・・　ボタンなど最小単位のコンポーネント  
├── const/　・・・　定数を定義するファイルを置くフォルダ  
├── features/　・・・　特定の機能などをまとめたフォルダ。この中にも複数のコンポーネントが存在する  
├── lib/　・・・　ライブラリなど  
├── pages/　・・・　ページ（デフォルトのもの）  
└── styles/　・・・　サイト内全体で使う共通CSS  

## 演算子
* 比較演算子  
    * 厳密等価演算子（===）  
    左右の2つのオペランドを比較します。 同じ型で同じ値である場合に、trueを返します。  
    * 等価演算子（==）  
    2つのオペランドを比較します。  
* 論理演算子  
    * AND演算子（&&）  
    左辺の値の評価結果がtrueならば、右辺の評価結果を返します  
    * OR演算子（||）  
    左辺の値の評価結果がtrueならば、そのまま左辺の値を返します。

## 動的API
 