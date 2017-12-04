progressDialog - A Native Android Progress Dialog Plugin for Cordova
======================

Requirements
-------------
- Android 4 or higher
- Cordova 3.0 or higher

Installation
-------------
    cordova plugin add cordova-plugin-progressdialog
    
Simple Usage
-------------
show:

    cordova.plugin.progressDialog.init({
        theme : 'HOLO_DARK',
        progressStyle : 'SPINNER',
        cancelable : true,
        title : 'Please Wait...',
        message : 'Contacting server ...',
        autoHide:3000
    });

dismiss:

    cordova.plugin.progressDialog.dismiss();


Functions
----------

###.init(_arguments_)

Initialize the progress dialog and set various parameters.
These are the valid options:

`theme`: can be one of the following:
`TRADITIONAL`, `DEVICE_DARK`, `DEVICE_LIGHT` (default), `HOLO_DARK`, `HOLO_LIGHT`


`progressStyle`: can be one of the following:
`SPINNER` (default), `HORIZONTAL`

`cancelable`: `true` (default) or `false`

`title`: title of the progress dialog (defaults to empty)

`message`: contents of the progress dialog (defaults to empty)

`autoHide`:can hide automatically

    cordova.plugin.progressDialog.init({
        theme : 'HOLO_DARK',
        progressStyle : 'SPINNER',
        cancelable : true,
        title : 'Please Wait...',
        message : 'Contacting server ...',
        autoHide:3000
    });

###.dismiss()

Dismiss the progress dialog.

    cordova.plugin.progressDialog.dismiss();

###.setProgress(_int_)

Set the value of the progress bar when progressStyle is `HORIZONTAL`.
    
    cordova.plugin.progressDialog.init({progressStyle : 'HORIZONTAL', title: 'Please Wait...', message : 'Connecting to server...'});
    cordova.plugin.progressDialog.setProgress(25);
    
![pDialog2](http://i.imgur.com/7k2docz.png)


###.setTitle(_title_)

Set the title of the progress dialog.
    
    cordova.plugin.progressDialog.setTitle('Please Wait...');
    
###.setMessage(_message_)

Set the message of the progress dialog

    cordova.plugin.progressDialog.setMessage('Connecting to server...');   
    
###.setCancelable(_boolean_)

Set whether the progress dialog is calncelable or not (defaults to `true`)

    cordova.plugin.progressDialog.setCancelable(false); // The user can not cancel the progress dialog  
    

Chaining The Functions
-----------------------

It is also possible to chain the functions instead of calling them one by one.

    cordova.plugin.progressDialog.init({
        theme: 'HOLO_DARK',
        title: 'Please Wait...',
        message : 'Connecting to server1...',
        progressStyle: 'HORIZONTAL',
        autoHide:3000
    })
    .setProgress(25)
    .setMessage('Connecting to server2...');

LICENSE
--------
The MIT License (MIT)

Copyright (c) 2017 bluebluesky

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

    