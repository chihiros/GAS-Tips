# Google SpredSheetsでGASを使ったマクロを作るときのメモ
## セルの値を取得する場合
```js
// 対処のシートを選択する
const sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName('対処のシート名');

// 対象とするセルの範囲を指定する
const cell = sheet.getRange('A2');
// or const cell = sheet.getRange(1, 2); // 1行目2列を意味する

// セルの値を取得する
const value = cell.getValue();

// 複数の場合
// 対象とするセルの範囲が複数の場合指定する
const cells = sheet.getRange('B1:D3');
// or const cell = sheet.getRange(2, 1, 2, 3); // 2行目1列から2行と3列の範囲を意味する

// セルの値を取得する
const values = cells.getValues();
```

## セルに値をセットする場合
```js
// 対処のシートを選択する
const sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName('対処のシート名');

// 対象とするセルの範囲を指定する
const cell = sheet.getRange('A2');
// or const cell = sheet.getRange(1, 2); // 1行目2列を意味する

// セルの値を取得する
const value = cell.setValue();
```
