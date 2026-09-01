# Overview

[简体中文](overview.zh-CN.md) | [Docs Index](README.md)

## Purpose

WebSocket frame, handshake, pipeline handlers, and permessage-deflate support for Gnalloy.

This module sits above transports and below application handlers. It translates bytes or Gnalloy messages into protocol objects, and translates outbound protocol objects back to bytes. It does not open sockets or own EventLoops.

## Repository Identity

- Module path: `gnalloy.org/codec-websocket`
- GitHub repository: `github.com/gnalloy/codec-websocket`
- Default branch: `dev`
- License: Apache-2.0

## Package Map
- `gnalloy.org/codec-websocket` (`websocket`)
- `gnalloy.org/codec-websocket/deflate` (`deflate`)

## Direct Gnalloy Dependencies
- `gnalloy.org/gnalloy`
- `gnalloy.org/codec-http1`
- `gnalloy.org/handler-timeout`

## Direct Dependents in the Current Module Plan
- `gnalloy.org/examples`
- `gnalloy.org/recipes`

## Architecture Position

Gnalloy keeps the core small and dependency-light. This repository is a replaceable module around one responsibility, connected through explicit Go packages instead of runtime discovery.

## Compatibility

The public import path is `gnalloy.org/codec-websocket`. Until the first stable tag is published, use `@dev` or an explicit pseudo-version selected by your dependency policy.
