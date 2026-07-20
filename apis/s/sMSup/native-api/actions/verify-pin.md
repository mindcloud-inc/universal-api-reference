# Verify PIN with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/2fa/verify`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Verify PIN](https://app.smsup.es/api/3.0/docs/2factor/verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msisdn` | body | `string` | yes | Mobile number that previously requested verification. |
| `pin` | body | `string` | yes | Verification PIN received by the user. |
