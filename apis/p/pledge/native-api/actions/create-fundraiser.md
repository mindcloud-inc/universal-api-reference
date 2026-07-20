# Create Fundraiser with Pledge

Creates a fundraiser in Pledge.

## Endpoint

- **Method:** `POST`
- **Path:** `/fundraisers`
- **Base URL:** `https://api.pledge.to/v1`
- **Official documentation:** [Create Fundraiser](https://developer.pledge.to/api/#tag/Fundraisers/operation/createFundraiser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beneficiary.id` | body | `string` | yes | Organization ID for the fundraiser beneficiary. |
| `goal` | body | `string` | no | Fundraising goal amount. |
| `start_time` | body | `string` | no | Event start time in ISO 8601 format. |
| `end_time` | body | `string` | no | Event end time in ISO 8601 format. |
