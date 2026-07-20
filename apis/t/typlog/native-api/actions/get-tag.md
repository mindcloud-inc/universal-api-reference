# Get Tag with Typlog

Retrieves a Typlog tag by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Get Tag](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the tag. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
