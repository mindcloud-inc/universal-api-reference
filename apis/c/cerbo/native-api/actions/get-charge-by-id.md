# Get Charge By ID with Cerbo

Retrieves charge details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/charges/:charge_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Charge By ID](https://docs.cer.bo/#tag/Charges/operation/showChargeById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `charge_id` | path | `number` | yes | The ID of the charge to retrieve. |
| `include_deleted` | query | `boolean` | no | If true, will return the charge even if it has been deleted. Useful for retrieving historical records. |
