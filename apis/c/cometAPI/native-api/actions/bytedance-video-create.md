# Bytedance Video Create with CometAPI

Creates a ByteDance video task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/volc/v3/contents/generations/tasks`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Bytedance Video Create](https://apidoc.cometapi.com/api/video/bytedance/bytedance-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `object` | yes | Bytedance content payload. |
| `model` | body | `string` | yes | Bytedance model identifier. |
