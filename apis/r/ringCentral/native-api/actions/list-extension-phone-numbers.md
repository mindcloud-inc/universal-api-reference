# List Extension Phone Numbers with RingCentral

Retrieves phone numbers for a RingCentral extension.

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/extension/:extensionId/phone-number`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [List Extension Phone Numbers](https://developers.ringcentral.com/api-reference/Phone-Numbers/listExtensionPhoneNumbers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `extensionId` | path | `string` | yes |
