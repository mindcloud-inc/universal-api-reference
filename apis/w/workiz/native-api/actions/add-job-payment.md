# Add Job Payment with Workiz

Adds a payment to a job in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/job/addPayment/:UUID/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Add Job Payment](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Payment amount. |
| `date` | body | `string` | yes | Date and time when payment was made. |
| `reference` | body | `string` | no | Optional confirmation number or reference. |
| `type` | query | `string` | yes | The type of payment. |
| `UUID` | path | `string` | yes | The job UUID. |
