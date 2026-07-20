# List Monitors By Cursor with Parallel Web Systems

## Endpoint

- **Method:** `GET`
- **Path:** `/v1alpha/monitors/list`
- **Base URL:** `https://api.parallel.ai`
- **Official documentation:** [List Monitors By Cursor](https://docs.parallel.ai/api-reference/monitor/list-monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Opaque pagination cursor returned by a previous list response. |
| `limit` | query | `number` | no | Maximum number of monitors to return. |
