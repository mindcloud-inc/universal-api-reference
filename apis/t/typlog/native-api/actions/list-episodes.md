# List Episodes with Typlog

Retrieves episodes from Typlog.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [List Episodes](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `cursor` | query | `number` | no | Pagination cursor. |
| `search` | query | `string` | no | Search term. |
