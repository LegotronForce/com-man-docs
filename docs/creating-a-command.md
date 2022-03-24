# Creating A Command
Creating a command in `ComMan` is relatively simple. All commands are really JS Objects with a few tags including `name`, `aliases`,
and `onCall`. You can start from scratch or use a template, but for this tutorial I'll be using the template. First thing's first,
you'll want to download the template and put it into the `commands` folder (it should be right outside the main directory). Then, you'll want
to open it in your favorite text editor (I use Visual Studio Code). Once you open the file, you should see something like this:
```js
module.exports = {
    name: 'command_name_here',
    alias: [],

    helpPage: {
        title: 'command_name_here',
        description: 'command_desc_here',
        synopsis: 'command_synopsis_here',
        arguments: []
    },

    onCall: function(logger, args) {
    }
};
```

To begin, let's look at `name`.The `name` tag is the string that shows what command it is. If the `name` is `test`, it'll run if you type in `test`.
Next is `alias`. Basically, it's other names that call the same function (in this case, `onCall`). After that is `helpPage`, which is used to display
some information about the command. Note that it is not necessarily required, however it is strongly recommended. Finally, but definitely not least,
is the `onCall` function. It is called whenever you call the command, and has two arguments: the `logger` (which is `Log4Water:EXPANDED`), and `args`
(the arguments of the command).

Let's begin with a simple command... perhaps a `Hello, world`. To begin, change the text for `name` to be `helloworld`. To simplify this
"lesson," we'll not worry about `helpPage`, so let's skip that and go to `onCall`. There, it is highly recommended to use `Log4Water:EXPANDED`,
so I'll be showing it here. We type in the following in `onCall`:
```js
onCall: function(logger, args) {
  logger.log("Hello, world!");
}
```
and there you go. You know have a (hopefully) working command. And if you want to see the final code, look down here:
```js
module.exports = {
  name: 'command_name_here',
  alias: [],

  helpPage: {
      title: 'command_name_here',
      description: 'command_desc_here',
      synopsis: 'command_synopsis_here',
      arguments: []
  },
  
  onCall: function(logger, args) {
    logger.log("Hello, world!");
  }
};
```
