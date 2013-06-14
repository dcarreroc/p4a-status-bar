P4A Status Bar
==============

This is a small modification for p4a default mask.

Open **/p4a/themes/default/mask/default/default.php** find `<div id="p4a_footer">` and add the [following code](https://github.com/dcarreroc/p4a-status-bar/blob/master/status_bar.php) before.

In your P4A Class you can add the code:

```php
    $this->build("P4A_Box", "status_bar_box");
    $this->box_stick->setHtml("<strong>".date("d/m/Y")."</strong><strong>IP:</strong>".$_SERVER['REMOTE_ADDR']);
``` 
Then in your P4A_Mask:

```php
    $this
       ->display("menu", P4A::singleton()->menu)
       ->display("status_bar", P4A::singleton()->status_bar_box);
``` 

Example of result:

<img src="http://daniel.carrero.cl/images/p4a_status_bar/sample.png" />
