# Verify Number Format with SMSEdge

Verifies phone number format in SMSEdge.

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/number-simple/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Verify Number Format](https://developers.smsedge.io/reference/verify-number-simple)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_id` | query | `string` | no | ID of country. Recommended to specify this parameter if phone number is local format |
| `number` | query | `string` | yes | Phone number that should be verified |
