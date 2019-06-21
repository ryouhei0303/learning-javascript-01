# learning-javascript-01

テクノロジー（藤原）JavaScriptの練習 (1)

## Q1の回答「コメントを解除したことで、どう変化しましたか？」

【こんにちはと返ってきた】

## Q2の回答「エラーの原因は何でしょうか？（調べてみましょう）」

【 SSR の影響で window とか document を使うとエラーが出るらしい。】

## Chromeデベロッパーツール：Consoleの実行結果

```
【おはよう！
index.html:56 Live reload enabled.
:5500/favicon.ico:1 Failed to load resource: the server responded with a status of 404 (Not Found)
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:53 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:53
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:1 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
index.html:18 おはよう！
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:18 おはよう！
index.html:52 [Intervention] Blocked attempt to show a 'beforeunload' confirmation panel for a frame that never had a user gesture since its load. https://www.chromestatus.com/feature/5082396709879808
socket.onmessage @ index.html:52
Navigated to http://127.0.0.1:5500/learning-javascript-01/index.html
index.html:18 おはよう！】
```

## ターミナルの実行結果

```
【shintaniryouheinoMacBook-Pro:~ shintaniryouhei$ cd ~/fujiwara
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ git clone git@github.com:ryouhei0303/learning-javascript-01.git
Cloning into 'learning-javascript-01'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 10 (delta 0), reused 7 (delta 0), pack-reused 0
Receiving objects: 100% (10/10), done.
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ code .
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
-bash: node: command not found
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ cat ~/.bash_profile
if [ -f ~/.bashrc ]; then
  . ~/.bashrc
fi

# Setting PATH for Python 3.7
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.7/bin:${PATH}"
export PATH
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ curl -L git.io/nodebrew | perl - setup
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
  0     0    0     0    0     0      0      0 --:--:--  0:00:01 --:--:--     0
100 24634  100 24634    0     0  12507      0  0:00:01  0:00:01 --:--:-- 12507
Fetching nodebrew...
Installed nodebrew in $HOME/.nodebrew

========================================
Export a path to nodebrew:

export PATH=$HOME/.nodebrew/current/bin:$PATH
========================================
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ echo "export PATH=$HOME/.nodebrew/current/bin:$PATH" >> ~/.bashrc
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ source ~/.bashrc
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ nodebrew
nodebrew 1.0.1

Usage:
    nodebrew help                         Show this message
    nodebrew install <version>            Download and install <version> (from binary)
    nodebrew compile <version>            Download and install <version> (from source)
    nodebrew install-binary <version>     Alias of `install` (For backward compatibility)
    nodebrew uninstall <version>          Uninstall <version>
    nodebrew use <version>                Use <version>
    nodebrew list                         List installed versions
    nodebrew ls                           Alias for `list`
    nodebrew ls-remote                    List remote versions
    nodebrew ls-all                       List remote and installed versions
    nodebrew alias <key> <value>          Set alias
    nodebrew unalias <key>                Remove alias
    nodebrew clean <version> | all        Remove source file
    nodebrew selfupdate                   Update nodebrew
    nodebrew migrate-package <version>    Install global NPM packages contained in <version> to current version
    nodebrew exec <version> -- <command>  Execute <command> using specified <version>

Example:
    # install
    nodebrew install v8.9.4

    # use a specific version number
    nodebrew use v8.9.4
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ nodebrew install-binary latest
v12.4.0 is already installed
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ nodebrew ls
v12.4.0

current: v12.4.0
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ nodebrew use latest
use v12.4.0
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
internal/modules/cjs/loader.js:626
    throw err;
    ^

Error: Cannot find module '/Users/shintaniryouhei/Documents/fujiwara/node-main.js'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:623:15)
    at Function.Module._load (internal/modules/cjs/loader.js:527:27)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
internal/modules/cjs/loader.js:626
    throw err;
    ^

Error: Cannot find module '/Users/shintaniryouhei/Documents/fujiwara/node-main.js'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:623:15)
    at Function.Module._load (internal/modules/cjs/loader.js:527:27)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
internal/modules/cjs/loader.js:626
    throw err;
    ^

Error: Cannot find module '/Users/shintaniryouhei/Documents/fujiwara/node-main.js'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:623:15)
    at Function.Module._load (internal/modules/cjs/loader.js:527:27)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
internal/modules/cjs/loader.js:626
    throw err;
    ^

Error: Cannot find module '/Users/shintaniryouhei/Documents/fujiwara/node-main.js'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:623:15)
    at Function.Module._load (internal/modules/cjs/loader.js:527:27)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
internal/modules/cjs/loader.js:626
    throw err;
    ^

Error: Cannot find module '/Users/shintaniryouhei/Documents/fujiwara/node-main.js'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:623:15)
    at Function.Module._load (internal/modules/cjs/loader.js:527:27)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ node node-main.js
internal/modules/cjs/loader.js:626
    throw err;
    ^

Error: Cannot find module '/Users/shintaniryouhei/Documents/fujiwara/node-main.js'
    at Function.Module._resolveFilename (internal/modules/cjs/loader.js:623:15)
    at Function.Module._load (internal/modules/cjs/loader.js:527:27)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ ls
hello-git		learning-javascript-01	simple-web-site
learning-http-message	sample-web-server
shintaniryouheinoMacBook-Pro:fujiwara shintaniryouhei$ cd learning-javascript-01/
shintaniryouheinoMacBook-Pro:learning-javascript-01 shintaniryouhei$ node node-main.js
/Users/shintaniryouhei/Documents/fujiwara/learning-javascript-01/node-main.js:1
window.alert("Hello, Node.js!!");
^

ReferenceError: window is not defined
    at Object.<anonymous> (/Users/shintaniryouhei/Documents/fujiwara/learning-javascript-01/node-main.js:1:1)
    at Module._compile (internal/modules/cjs/loader.js:774:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:785:10)
    at Module.load (internal/modules/cjs/loader.js:641:32)
    at Function.Module._load (internal/modules/cjs/loader.js:556:12)
    at Function.Module.runMain (internal/modules/cjs/loader.js:837:10)
    at internal/main/run_main_module.js:17:11
shintaniryouheinoMacBook-Pro:learning-javascript-01 shintaniryouhei$ node node-main.js
Goodmorning, Node.js!!
shintaniryouheinoMacBook-Pro:learning-javascript-01 shintaniryouhei$ 】
```

