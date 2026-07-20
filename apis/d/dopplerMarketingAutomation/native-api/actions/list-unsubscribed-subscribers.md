# List Unsubscribed Subscribers with Doppler Marketing Automation

Retrieves unsubscribed subscribers from Doppler Marketing Automation.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountName/unsubscribed`
- **Base URL:** `https://restapi.fromdoppler.com`
- **Official documentation:** [List Unsubscribed Subscribers](https://restapi.fromdoppler.com/docs/rels/get-unsubscribed-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | Inclusive start date-time filter. Doppler returns a gateway error without a date window. |
| `to` | query | `date` | yes | Exclusive end date-time filter. Doppler returns a gateway error without a date window. |
