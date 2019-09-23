## 課題1の解答

スプレッド演算子を使用して変数 `new_x_menbers` に `x_menbers` を代入して `HEATH` と `SUGIZO` を追加します。

```javascript
const x_members = ['YOSHIKI', 'TOSHI', 'HIDE', 'PATA', 'TAIJI'];
const new_x_members = [...x_members, 'HEATH', 'SUGIZO'];
console.log(new_x_members);
```

- [スプレッド構文 - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

```javascript
// スプレッド演算子を使わない例：concatを使って結合する
const x_menbers = ['YOSHIKI', 'TOSHI', 'HIDE', 'PATA', 'TAIJI']
const add_menbers = ['HEATH', 'SUGIZO']
const new_x_menbers = x_menbers.concat(add_menbers)
console.log(x_menbers)
console.log(new_x_menbers)
```

- [Array.prototype.concat() - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)

## 課題2の解答

array.map()を使い新しい配列を作り戻り値に `toUpperCase` メソッドを使います。

```javascript
const x_members = ['YoShIKi', 'ToShI', 'HIdE', 'paTA', 'TAiJI', 'hEAtH', 'SUGIzo']
const upper_member_names = x_members.map(val => val.toUpperCase())
console.log('元の配列 ' + x_members)
console.log('新しい配列 ' + upper_member_names)
```

- [Array.prototype.map() - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
- [String.prototype.toUpperCase() - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)

## 課題3の解答

array.sort()を使い比較関数で昇順にします。  
sortメソッドは元の配列を変更してしまうので、sliceで配列をコピーします。  
元の配列は変更しないようにしましょう。

### 比較関数

配列の要素は比較関数の返り値に基づきソートされます。

- 0より小さい − aはbの前に来る
- 0より大きい − bはaの前に来る
- 0に等しい − aとbは変更されない

### 参考

- [Array.prototype.sort() - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)
- [Array.prototype.slice() - JavaScript | MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)

```javascript
const numbers = [5, 6, 4, 2, 10, 44, 33, 30, 50, 1, 999, 79, 48, 66]
const sort_numbers = numbers.slice().sort((a, b) => a - b)
console.log('元の配列 ' + numbers)
console.log('sortした配列 ' + sort_numbers)
```