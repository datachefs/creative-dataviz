---
title: Scripting Talon
layout: content
# image: cookies-dataviz.jpg
---


- error log

-  zap: key(backspace), killed: key(delete), zoom: pageup/pagedown

zap <number>: key("backspace:{number}")

```
ctx.lists["user.listname"] = ["word", "word2"]
ctx.lists["user.listname"] = {
    "pronunciation": "word",
}
```

```
from talon import Module, Context

mod = Module()
mod.list("exception_class", desc="Exception classes")

ctx_default = Context()
ctx_default.lists["user.exception_class"] = {
    "generic exception": "Exception"
}

contexts. Note also that our list (like user defined actions) is prefixed with user. to identify it as custom code.

exceptions.talon:

exception {user.exception_class}: insert(user.exception_class)

```

- Adding list into insert: some_command <user.text>: insert("command {text}\n")
- shuffle  control <user.letter>:     insert("key(ctlr-{letter})")
- curl Tab 3: key("tab:3")
- go tab <number>: key(number)
- select all: key(ctrl-a)
-  sleep(100ms)
- (pace |  paste) all
-  press <user.key>:  key(keys)  # NOTE: is it key or keys?
- <User.letter>
- NOTE: knausj tends not to use a key directly, since different platforms use different keys; if you are doing it for yourself you can just use whatever works for you



Sample keys:
- swap: key(alt-tab)


 ## Context

- app: Outlook
-  other Common apps: Slack
- App names:  I think registry.decls.apps, but please do not use that in business logic in code, the registry is only available for debugging purposes
- App names:  I think registry.decls.apps, but please do not use that in business logic in code, the registry is only available for debugging purposes
- title: /gmail/


## Troubleshooting
- start with sim("say function round") in the repl to see which rule is matching



```
mod.list("git_command", desc="Git commands.")
mod.list("git_argument", desc="Command-line git options and arguments.")

dirpath = Path(__file__).parent
arguments_csv_path = str(dirpath / "git_arguments.csv")
commands_csv_path = str(dirpath / "git_commands.csv")

```