# ClientsideTimer
Clientside Timer for GTANetwork

---

### How to use it:


##### Base Code
```
API.onChatMessage.connect(function (msg) {
    if (msg === "hello") {
        var timer: Timer = resource.Timer.newTimer(5000, resource.your_file_name.testFunction);
        timer.Running = true;
        timer.RunOnce = true;
    }
});

function testFunction() {
    API.sendChatMessage("Hello World");
}
```

Initialize a timer:
`var timer: Timer = resource.Timer.newTimer(x, function);`
`x = Time in milliseconds before we run the function.`
`function = The function you want to run.` EX. `resource.myFileName.myFunction;`

Start your timer.
`timer.Running = true`

Run it endlessly until you tell it to stop.
`timer.RunOnce = false`

Add some aguments to your function.
`var args: any[] = ["Argument1", argument2, 2]`
`timer.Args = args;`
