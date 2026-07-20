# Update or Cancel Review with Shopper Approved

Updates or cancels a review in Shopper Approved.

## Endpoint

- **Method:** `PUT`
- **Path:** `/reviews/:siteid/:reviewid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [Update or Cancel Review](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewid` | path | `string` | yes | The review ID or order ID. |
| `followup` | body | `date` | no | The follow-up date in YYYY-MM-DD format. |
| `cancel` | body | `number` | no | Set to 1 to cancel the review. |
