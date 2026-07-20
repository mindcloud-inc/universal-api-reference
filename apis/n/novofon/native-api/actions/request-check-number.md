# Request Check Number with Novofon

Creates a number check request in Novofon.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/request/checknumber/`
- **Base URL:** `https://api.novofon.com`
- **Official documentation:** [Request Check Number](https://novofon.com/instructions/api/#checknumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caller_id` | query | `string` | yes | Caller ID number displayed for the validation call. Only numbers already connected in Novofon are allowed. |
| `code` | query | `string` | no | Optional numeric code to play during the validation call. |
| `to` | query | `string` | yes | Phone number or SIP destination to validate. |
