# Find Link By Path And Domain with lc.cx

Finds a short link in lc.cx by path and domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/links`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Find Link By Path And Domain](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | The shortlink path to look up. |
| `domain` | query | `string` | yes | The domain ID that owns the requested path. |
