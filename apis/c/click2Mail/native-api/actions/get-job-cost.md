# Get Job Cost with Click2Mail

Retrieves job cost details from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/jobs/{id}/cost`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Get Job Cost](https://developers.click2mail.com/reference/getjobcost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | job id |
| `details` | query | `string` | no | Returns the cost break down |
| `paymentType` | query | `string` | no | Default is Credit Card |
| `couponCode` | query | `string` | no | Coupon Code |
