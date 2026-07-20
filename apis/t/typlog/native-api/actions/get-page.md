# Get Page with Typlog

Retrieves a Typlog page by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/pages/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Get Page](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the page. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
