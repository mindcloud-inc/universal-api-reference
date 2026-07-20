# Verify Email with NeverBounce

Verifies an email address in NeverBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/single/check`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Verify Email](https://developers.neverbounce.com/reference/single-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to verify. |
| `address_info` | query | `boolean` | no | Include parsed address details in the verification response. |
| `credits_info` | query | `boolean` | no | Include credit usage details in the verification response. |
| `timeout` | query | `number` | no | Maximum verification time before returning an unknown result. |
