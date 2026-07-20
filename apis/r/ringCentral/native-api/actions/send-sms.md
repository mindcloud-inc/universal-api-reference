# Send SMS with RingCentral

Sends an SMS message from a RingCentral extension.

## Endpoint

- **Method:** `POST`
- **Path:** `restapi/v1.0/account/:accountId/extension/:extensionId/sms`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [Send SMS](https://developers.ringcentral.com/api-reference/SMS/createSMSMessage)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `extensionId` | path | `string` | yes |
| `from.phoneNumber` | body | `string` | yes |
| `to.phoneNumber[]` | body | `array<string>` | yes |
| `country.isoCode` | body | `string` | no |
| `text` | body | `string` | yes |
