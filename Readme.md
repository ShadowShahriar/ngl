# Overview

tl;dr

> I made my personal NGL (sort of).

# What is NGL?

> [NGL][1] is a mobile app available for both Android and iOS that allows users to send one another anonymous messages. It integrates like an add-on for Instagram to share the responses directly to their stories.

Most of my college friends have started using this app to send private messages. It is like a fun game where you can say and ask basically anything and get witty responses. I really wanted to try this thing. However, I wouldn't prefer to install another app just to receive anonymous messages. I thought, why bother installing when I can make my own NGL?

Now my friends can send me private messages by visiting: **https://shadowshahriar.github.io/ngl**

# How does it work?

The main page uses an HTML form with an `action` attribute. The `action` attribute sends a `GET` request to my Cloudflare Worker located at **https://ngl.shadowshahriar.workers.dev**. Since the form has only one input field (`textarea`), it sends the textarea content in the URL string.

The Cloudflare Worker receives the message, checks if it was sent from my GitHub pages, and sends it to [**my Telegram bot**][2].

# License

The source code is licensed under [MIT][3].

[1]: https://ngl.link/
[2]: https://t.me/emmy_the_robot
[3]: https://github.com/ShadowShahriar/ngl/blob/main/LICENSE
