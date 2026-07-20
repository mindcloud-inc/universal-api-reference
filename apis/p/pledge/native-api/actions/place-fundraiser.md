# Place Fundraiser with Pledge

Updates fundraiser placement in Pledge.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fundraisers/[:id]`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Place Fundraiser](https://developer.pledge.to/api/#tag/Fundraisers/operation/placeFundraiser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Fundraiser ID. |
| `beneficiary.id` | body | `string` | yes | Organization ID for the fundraiser beneficiary. |
| `goal` | body | `string` | no | Fundraising goal amount. |
| `start_time` | body | `string` | no | Event start time in ISO 8601 format. |
| `end_time` | body | `string` | no | Event end time in ISO 8601 format. |
