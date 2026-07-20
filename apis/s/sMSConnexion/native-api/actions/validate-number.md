# Validate Number with SMS Connexion

Validates a phone number in SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/validate/:phoneNumber`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Validate Number](https://sms.cx/sms-api-documentation/#operation/ValidateNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | Phone number in E.164 format, e.g. +4915123772462. |
