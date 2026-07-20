# Set Post Status with Typlog

Updates the status of a Typlog post.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/[:id]/status`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Set Post Status](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the post. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `status` | body | `string` | no | Target post status. |
| `published_at` | body | `date` | no | Publish timestamp for scheduled or published posts. |
