# Midjourney Submit Action with CometAPI

Creates a Midjourney action task in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/mj/submit/action`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Midjourney Submit Action](https://apidoc.cometapi.com/api/image/midjourney/action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customId` | body | `string` | yes | Midjourney custom action identifier. |
| `taskId` | body | `string` | yes | Midjourney task identifier. |
