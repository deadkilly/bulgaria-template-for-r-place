# bulgaria-template-for-r-place
За сега има само една снимка, така че няма нужда от файлове в repository-то. 
За да set up-нете (чрез Chrome само!):
1. Свалете това: https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en
2. Натисни върху extension-а
3. "Create new script"
4. Копи-пейст този код (върху целия файл): 
```
 'use strict';

    // ==UserScript==
    // @name         r/bulgaria ABV
    // @namespace    http://tampermonkey.net/
    // @version      0.3.1
    // @description  try to take over the canvas!
    // @author       wokstym - repurposed from other subreddits
    // @match        https://hot-potato.reddit.com/embed*
    // @icon         https://www.google.com/s2/favicons?sz=64&domain=reddit.com
    // @grant        none
    // ==/UserScript==
if (window.top !== window.self) {
    window.addEventListener('load', () => {
            document.getElementsByTagName("mona-lisa-embed")[0].shadowRoot.children[0].getElementsByTagName("mona-lisa-canvas")[0].shadowRoot.children[0].appendChild(
        (function () {
            const i = document.createElement("img");
            i.src = "https://i.imgur.com/cwM4dYo.png";
            i.style = "position: absolute;left: 0;top: 0;image-rendering: pixelated;width: 1000px;height: 1000px;";
            console.log(i);
            return i;
        })())

    }, false);

}
```

6. После save: ctrl + s
7. Накрая refresh reddit

https://i.imgur.com/AVZKys4.png

**Снимка от Gigo_G#3450 и код от Wokstym в github https://gist.github.com/Wokstym/1f296a181cd96a8fcf2b2dd1df65d9fa#file-r_poland_official_script-md** 
