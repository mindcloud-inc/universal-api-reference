# Set Episode Status with Typlog

Updates the status of a Typlog episode.

## Endpoint

- **Method:** `POST`
- **Path:** `/episodes/[:id]/status`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Set Episode Status](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the episode. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `status` | body | `string` | no | Target episode status. |
| `published_at` | body | `date` | no | Publish timestamp for scheduled or published episodes. |
