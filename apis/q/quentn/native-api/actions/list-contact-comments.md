# List Contact Comments with Quentn

## Endpoint

- **Method:** `GET`
- **Path:** `/contact/:contact_id/comments`
- **Base URL:** `https://tbg6y3.us-1.quentn.com/public/api/v1`
- **Official documentation:** [List Contact Comments](https://help.quentn.com/hc/en-150/articles/4517835330961-Contact-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | Numeric Quentn contact id. |
| `range` | query | `number` | no | Zero-based comment range offset. Default is 0. |
| `limit` | query | `number` | no | Maximum number of comments to return. Default is 50 and upper limit is 50. |
| `sort` | query | `string` | no | Sort order for the comments response. |
