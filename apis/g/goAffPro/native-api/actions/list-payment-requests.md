# List Payment Requests with GoAffPro

Retrieves affiliate payment requests from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/payments/requests`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Payment Requests](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return payment requests for this affiliate ID. |
| `status` | query | `string` | no | Only return payment requests with this status. |
