---
description: ''
sidebar: 'editor'
author: 'solveddev'
next: '/plugin-docs/'
prev: '/editor-docs/no-cache/'
---

# MoLang

A fast MoLang parser used and developed by the bridge. team.

## About

> MoLang is a simple expression-based language designed for fast calculation of values at run-time. Its focus is solely to enable script-like capabilities in high-performance systems where JavaScript is not performant at scale. We need scripting capabilities in these low-level systems to support end-user modding capabilities, custom entities, rendering, and animations.

\- From the Minecraft documentation

## Installation

-   `npm i molang`

    **or**

-   Download the `dist/main.web.js` file and add the script to your HTML page (library access via global `MoLang` object).

## Usage

```javascript
import { MoLang } from 'molang'

const molang = new MoLang(
	{
		query: {
			x: 0,
			get(val) {
				return val + 4
			},
		},
	},
	{ useCache: true }
)
molang.execute('query.x + query.get(3) == 7')
```

## MoLang Playground

We have built a very basic MoLang playground with this parser. You can use it at [bridge-core.github.io/molang-playground](https://bridge-core.github.io/molang-playground).
