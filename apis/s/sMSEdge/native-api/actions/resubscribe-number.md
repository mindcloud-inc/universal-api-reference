# Resubscribe Number with SMSEdge

Resubscribes a phone number in SMSEdge.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/numbers/remove-unsubscriber`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Resubscribe Number](https://developers.smsedge.io/reference/resubscribe-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Country ISO or country ID when needed for local numbers |
| `number` | query | `string` | yes | Phone to resubscribe |
