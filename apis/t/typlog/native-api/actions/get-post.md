# Get Post with Typlog

Retrieves a Typlog post by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Get Post](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the post. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
