# Google Drive Spreadsheet Script

### Reading Spreadsheet

```javascript
var spreadSheet = SpreadsheetApp.getActiveSpreadsheet();  
var sheet = spreadSheet.getSheets()[0]; // index start 0
var data = sheet.getDataRange().getValues();
for (var i = 1; i < data.length; i++) {
  var status = data[i][0];
}
```

### Writting

```javascript
var spreadSheet = SpreadsheetApp.getActiveSpreadsheet();  
var sheet = spreadSheet.getSheets()[4];
// Row, Column - starting at 1
sheet.getRange(3, 8).setValue();
```

### On edit

```javascript
function onEdit(e) {
  var currentRange = e.range;
  var currentSheet = currentRange.getSheet();
  // Column number = currentRange.getColumn()
}
```


### Utils

compare string regex:
```javascript
var result = RegExp(textToSearch).test(fullText);

// OR Index of
if (fullText.indexOf(textToSearch) > -1) {
``
