# Update Fundraiser with Pledge

Updates an existing fundraiser in Pledge.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/fundraisers/[:id]`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Update Fundraiser](https://developer.pledge.to/api/#tag/Fundraisers/operation/updateFundraiser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Fundraiser ID. |
| `goal` | body | `string` | no | Fundraising goal amount. |
| `start_time` | body | `string` | no | Event start time in ISO 8601 format. |
| `end_time` | body | `string` | no | Event end time in ISO 8601 format. |
