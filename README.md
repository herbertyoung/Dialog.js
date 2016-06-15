# Dialog.js
A JavaScript plugin simulating the native JavaScript functions: 'alert()' and 'confirm()'. In addition you can easily customize your popup windows.
## How to use?
### 1.Including files
```html
<link rel="stylesheet" href="./css/dialog.min.css">
<script src="./js/dialog.min.js"></script>
```
### 2.Calling the plugin
```html
<script>
    // simulate alert with title
    showAlert('title', 'content', function confirmHandler(){});
    // simulate alert without title
    showAlert('content', function confirmHandler(){});
    // simulate confirm with title
    showConfirm('title', 'content', function confirmHandler(){}, function cancel(){});
    // simulate confirm without title
    showConfirm('content', function confirmHandler(){}, function cancel(){});
</script>
```
