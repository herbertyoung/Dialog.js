# Dialog.js
A JavaScript plugin simulating the native JavaScript functions: `alert()` and `confirm()`. In addition you can easily customize your popup windows.

## Usage

### Including files
```html
<link rel="stylesheet" href="css/dialog.min.css">
<script src="js/dialog.min.js"></script>
```

### Calling the plugin

#### Show the `alert` popup window
```html
<script>
    showAlert('title', 'content', function confirmHandler(){});
</script>
```

#### Show the `confirm` popup window
```html
<script>
    showConfirm('title', 'content', function confirmHandler(){}, function cancelHandler(){});
</script>
```

## Customizing yourself a popup window
You can also customize yourself a popup window.

A popup window's html structure is:
```html
<div class="pop" style="display: none;" id="popDemo">
    <div class="pop-dialog">
        <div class="pop-content">
            <div class="pop-header">your title</div>
            <div class="pop-body">
            	<p>you can customize any content yourself as you like.</p>
            	<div>
            		<label>username</label><input type="text">
            	</div>
            </div>
            <div class="pop-footer">
                <div data-action="close" class="primary">close</div>
                <div>customized button</div>
            </div>
        </div>
    </div>
</div>
```

How to show this popup window? You can just using `data-*` attributes to show yours.

The `data-toggle="pop"` attribute means that show a pop up window.

The `data-target="#popDemo"` attribute means that which pop up window will be shown. 
```html
<button data-toggle="pop" data-target="#popDemo">show customized popup</button>
```

You can also customize your close button to hide you popup window using the `data-action="close"` attribute.
```html
<div data-action="close">close</div>
```

## Methods

### `Alert`

#### showAlert([title], content, [confirmHandler])
Show the `alert` popup window.

Parameters:
- title: String
- content: String
- confirmHandler: Function

#### hideAlert()
Hide the `alert` popup window.

### `Confirm`

#### showConfirm([title], content, [confirmHandler, [cancelHandler]])
Show the `confirm` popup window.

Parameters:
- title: String
- content: String
- confirmHandler: Function
- cancelHandler: Function

#### hideConfirm()
Hide the `confirm` popup window.