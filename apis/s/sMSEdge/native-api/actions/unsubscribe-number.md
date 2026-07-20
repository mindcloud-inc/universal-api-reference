# Unsubscribe Number with SMSEdge

Unsubscribes a phone number in SMSEdge.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/unsubscribe/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Unsubscribe Number](https://developers.smsedge.io/reference/unsubscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Country ISO or country ID when needed for local numbers |
| `number` | query | `string` | yes | Phone to unsubscribe |
