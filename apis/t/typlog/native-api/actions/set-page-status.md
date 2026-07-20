# Set Page Status with Typlog

Updates the status of a Typlog page.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/[:id]/status`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Set Page Status](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the page. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `status` | body | `string` | no | Target page status. |
| `published_at` | body | `date` | no | Publish timestamp for scheduled or published pages. |
