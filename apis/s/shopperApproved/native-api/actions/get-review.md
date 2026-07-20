# Get Review with Shopper Approved

Retrieves a review from Shopper Approved by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/reviews/:siteid/:reviewid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [Get Review](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewid` | path | `string` | yes | The review ID or order ID. |
| `removed` | query | `number` | no | Whether to include removed reviews. |
| `full_name` | query | `number` | no | Whether to include the reviewer's full last name. |
