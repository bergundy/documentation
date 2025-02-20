---
id: dataconverter
title: tctl v1.17 data-converter command reference
sidebar_label: dataconverter
description: How to use the tctl v1.17 dataconverter command
toc_max_heading_level: 4
keywords:
- cli
- cli reference
- tctl
- temporal
- temporal cli
- temporal server
tags:
- cli
- cli-reference
- tctl
- temporal
- temporal-cli
- temporal-server
---

<!-- THIS FILE IS GENERATED. DO NOT EDIT THIS FILE DIRECTLY -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

:::success Temporal CLI is now available!

The new [Temporal CLI](/cli) is available for use.

tctl v1.17 can still be used with Temporal Server version 1.20 and is expected to be compatible with Temporal Server version 1.21.

tctl is expected to be fully deprecated by Temporal Server version 1.22

:::

The `tctl dataconverter` command enables custom [Data Converter](/dataconversion#) operations.

- [tctl dataconverter web](#web)

## web

The `tctl dataconverter web` command specifies the WebSocket URL of a custom [Data Converter](/dataconversion#) to use with Temporal Web.

`tctl dataconverter web --web_ui_url <url>`

The following modifiers control the behavior of the command.

### --port

Specify a port for the WebSocket URL of a custom [Data Converter](/dataconversion#).
The default value is 0.

**Example**

```bash
tctl dataconverter web --web_ui_url <url> --port <value>
```

### --web_ui_url

_Required modifier_

Specify the WebSocket URL of a custom [Data Converter](/dataconversion#).

**Example**

```bash
tctl dataconverter web --web_ui_url <url>
```

