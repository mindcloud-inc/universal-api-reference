# Get Author with Typlog

Retrieves a Typlog author by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/authors/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Get Author](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the author. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
