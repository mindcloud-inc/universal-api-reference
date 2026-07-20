# Lookup Single Number with SMS Connexion

Looks up a phone number in SMS Connexion.

## Endpoint

- **Method:** `GET`
- **Path:** `/numbers/lookup/:phoneNumber`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Lookup Single Number](https://sms.cx/sms-api-documentation/#operation/LookupNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumber` | path | `string` | yes | Phone number in E.164 format, e.g. +33612246450. |
