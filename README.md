# c1220i1-module01-thang-mindmap

###Reflection 14/01

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<style>
    input {
        padding: 0 15px;
    }

    textarea {
        padding: 7px 0px;
    }

    fieldset {
        width: 20%;
    }

    textarea, button {
        margin-top: 10px;
    }
</style>
<fieldset>
    <legend>
        <p>Nokia</p>
    </legend>
    <p id="displaynokia">Pin:....%</p>
    <input type="text" placeholder="write messenger">
    <button onclick="nhap">Sent</button>
    <br>
    <textarea placeholder=" Hop thu di"></textarea><br>

    <textarea placeholder=" Hop Thu Den"></textarea>
    <br>
    <button>on</button>
    <button>Off</button>
    <button>Changer</button>
</fieldset>
<fieldset>
    <legend>
        <p>Iphone</p>
    </legend>
    <p id="displayiphone">Pin:....1%</p>
    <input type="text" placeholder="write messenger">
    <button onclick="nhap">Sent</button>
    <br>
    <textarea placeholder="Hop Thu Den"></textarea><br>

    <textarea placeholder="Hop Thu Den"></textarea>
    <br>
    <button>on</button>
    <button>Off</button>
    <button>Changer</button>
</fieldset>
<script>
    function mobile(name) {
        this.name = name;
        this.battery = 60;
        this.msg = '';
        this.inbox = [];
        this.outbox = [];
        this.mobileOn = function () {
            if (this.status) {
                alert('On')
            } else {
                alert('Off')
            }
        }
        this.onMobile = function () {
            this.status = true
        }
        this.offMobile = function () {
            this.status = false
        }
        this.charge = function (name) {
            this.battery++;
            setTimeout(function () {
                document.getElementById('displaynokia').innerText = 'pin' + nokia.battery;
            }, 2000)
            setTimeout(function () {
                document.getElementById('displayiphone').innerText = 'pin' + iphone.battery;
            }, 1000)
        }
        this.writeMsg = function () {
            this.msg = value;
        }
        this.sendMsg = function (mobile) {
            this.outbox.push(this.msg)
            mobile.reveiceMsg(this.msg, this.name)
            this.decreseBattery();
        }
        this.reveiceMsg = function (msg, name) {
            this.inbox.push(msg)
            alert('da nhan duoc tin nhan')
        }
        this.getBattery = function () {
            this.battery++;
        }
        this.decreseBattery = function () {
            this.battery--;
        }
    }

    let nokia = new mobile(nokia);
    let iphone = new mobile(iphone);
    display()

    function sendMsg(mobile1, mobile2) {
        mobile1.sendMsg(mobile2)
        display();
    }
    function display(){

    }
</script>
</body>
</html>
```