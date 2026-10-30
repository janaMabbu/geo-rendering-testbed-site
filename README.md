# GEO Rendering Testbed

A research website for studying how web rendering choices affect what AI crawlers and AI assistants can read.

**Live site:** https://geo-classic.vercel.app

## Why this exists

More and more people get answers from AI assistants such as ChatGPT, Claude, Perplexity, Gemini, Grok and Meta's Muse instead of clicking through search results. These systems learn about websites by fetching pages, and many of them read only the raw HTML a server sends. They do not run the JavaScript that a browser runs to fill in the page.

That means the way a site is rendered can decide whether an AI assistant ever sees its content. This project measures that effect under controlled conditions.

## What the site contains

The site serves the same set of product pages through six common Next.js rendering strategies:

| Strategy | In short |
|---|---|
| CSR | the browser builds the page with JavaScript |
| Blocking SSR | the server builds the whole page before sending it |
| SSG | pages are built once in advance |
| ISR | prebuilt pages that refresh every 60 seconds |
| Streaming SSR | the server sends the page in pieces as data becomes ready |
| PPR | a prebuilt shell, with changing parts streamed in |

**All products, brands, prices, reviews and figures on the site are fictional.** They do not describe real goods.

You can browse every page from [/browse](https://geo-classic.vercel.app/browse), and [/about](https://geo-classic.vercel.app/about) explains the project.

## What is logged

To study crawler behaviour, the site records standard request metadata: time, path, user agent and IP address. A small script reports whether a visitor ran JavaScript. There are no cookies, accounts or third party trackers. IP addresses are used only to verify which company a crawler belongs to, and results are reported in aggregate.

## Status

Data collection runs for 45 days. The full code, data and results will be published together with the research paper when the study is complete.

## Author

Janardhan (Jana) Mabbu
LinkedIn: https://www.linkedin.com/in/janardhan-mabbu-9626a1173

If you work on search, GEO or rendering architecture and have ideas about what to measure, I would like to hear from you.
