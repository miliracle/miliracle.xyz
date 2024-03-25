---
title: "The difference between `<script>`, `<script async>` and `<script defer>'"
date: 2024-03-25T22:07:11+07:00
draft: false
---

# The difference between `<script>`, `<script async>` and `<script defer>`

## **`<script>`**

The HTML content will be parsed till it hit the `<script>` tag → the HTML parsing will stop and the browser will start to fetch the script’s content → executing the script → then the HTML parsing will continue.

![script.png](/the-difference-between-script-script-async-and-script-defer/script.png)

## `<script async>`

The `async` keyword will tell the browser to download the script file then execute it when it is available. It won’t block the parsing process while downloading the script.

![async.png](/the-difference-between-script-script-async-and-script-defer/async.png)

## **`<script defer>`**

The `defer` keyword make the browser to download the script file when it is parsing the HTML, but will only execute it after the parsing process is completed, but before firing **`DOMContentLoaded`**

The `defer` scripts are also execute in the order as they appear in the document.

![defer.png](/the-difference-between-script-script-async-and-script-defer/defer.png)

> If the JavaScript code is not loaded from an external source (i.e., not specified by the `src` attribute), but instead included directly within the `<script>` tag, the browser will execute the script immediately when it encounters it during parsing → The `defer` attribute is ignored.
>