# Get Panel with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Panel/v3/ReadPanel`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Get Panel](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tenant` | body | `string` | yes | Tenant code for the panel request. |
| `panelId` | body | `number` | yes | Panel identifier to read. |
