<div align=center>
    <br>
    <p> 
        <a href="https://discord.gg/h7sVGsBaHP">
            <img src="https://img.shields.io/discord/798252971590025278?color=7289da&logo=discord&logoColor=white" alt="Discord">
        </a>
        <a href="https://www.npmjs.com/package/webhooks.js">
            <img src="https://img.shields.io/npm/v/webhooks.js.svg" alt="npm">
        </a>
        <a href="https://www.npmjs.com/package/webhooks.js">
            <img src="https://img.shields.io/npm/dt/webhooks.js.svg?maxAge=3600" alt="NPM downloads">
        </a>
    </p>
    <p>
        <a href="https://nodei.co/npm/webhooks.js/"><img src="https://nodei.co/npm/webhooks.js.png?downloads=true&stars=true" alt="npm installnfo" /></a>
    </p>
</div>

## Table of Contents
- [About](#about)
- [Installation](#installation)
- [Example](#example)
- [Links](#links)
- [Help](#help)

## About
Webhooks.js is a new, lightweight, and fast Node.js wrapper for the [Discord Webhooks](https://discord.com/developers/docs/resources/webhook) API.

- Object Oriented
- Up-to-Date

## Installation
**Node.js 12 or newer is required.**

`npm install webhooks.js --save`

## Examples
You can send a raw Webhook params object [Read More](https://discord.com/developers/docs/resources/webhook#execute-webhook-jsonform-params)

```js
const hooks = require('webhooks.js')
const hook = new hooks.Webhook({ id: "your-webhook-id", token: "your-webhook-token" })

hook.send({
    username: "Webhook",
    content: "Hello!",
    embeds: [{
        title: "hello!"
    }]
})
.then(json => {
    console.log(json)
})
.catch(err => {
    console.error(err)
})
```

or you can send a string

```js
const hooks = require('webhooks.js')
const hook = new hooks.Webhook({ id: "your-webhook-id", token: "your-webhook-token" })

hook.send("hello world!")
.then(json => {
    console.log(json)
})
.catch(err => {
    console.error(err)
})

```

or you can send a RichEmbed (different from [Discord.js MessageEmbeds](https://discord.js.org/#/docs/main/stable/class/MessageEmbed))

```js

const hooks = require('webhooks.js')
const hook = new hooks.Webhook({ id: "your-webhook-id", token: "your-webhook-token" })

const embed = new hooks.RichEmbed()
.setTitle(`Embed test`)
.setTimestamp()
.setDescription("Test..?")

hook.send(embed)
.then(json => {
    console.log(json)
})
.catch(err => {
    console.error(err)
})
```

## Links
- [Website](https://github.com/FHGDev/Webhooks.js)
- [Discord Server](https://discord.gg/mXN7ahsg9c)
- [NPM Package](https://npmjs.com/package/webhooks.js)

## Help
You can get help in the [Webhooks.js Discord Server](https://discord.gg/F8MDd4qTad) in the #support channel.
