# bookworm-template
Install extension

Chrome:
https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo?hl=en

Firefox
https://addons.mozilla.org/en-US/firefox/addon/violentmonkey/

open extension menu

![obraz](https://user-images.githubusercontent.com/37674089/161429963-323feeb3-bf73-48ea-814f-1e52c305fc8c.png)

 add script
 
![obraz](https://user-images.githubusercontent.com/37674089/161429974-7db89b8e-5593-44a4-b549-47af8f5f5403.png)


Copy script:
```
// ==UserScript==
// @name         Bookworm glico pose
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  Spread the love of HOLLOW LIFE
// @author       oralekin
// @match        https://hot-potato.reddit.com/embed*
// @icon         https://www.google.com/s2/favicons?sz=64&domain=reddit.com
// @grant        none
// ==/UserScript==
if (window.top !== window.self) {
    window.addEventListener('load', () => {
            document.getElementsByTagName("mona-lisa-embed")[0].shadowRoot.children[0].getElementsByTagName("mona-lisa-canvas")[0].shadowRoot.children[0].appendChild(
        (function () {
            const i = document.createElement("img");
            i.src = "https://raw.githubusercontent.com/ludrol/bookworm-template/main/Bookworm_place_template.png";
            i.style = "position: absolute;left: 0;top: 0;image-rendering: pixelated;width: 2000px;height: 1000px;";
            console.log(i);
            return i;
        })())

    }, false);

}
```

save script with ctrl + S

refresh https://www.reddit.com/r/place/?cx=1886&cy=875&px=16

