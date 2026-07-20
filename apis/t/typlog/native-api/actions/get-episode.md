# Get Episode with Typlog

Retrieves a Typlog episode by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Get Episode](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the episode. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
