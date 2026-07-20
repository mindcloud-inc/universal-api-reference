# List Extensions with RingCentral

Retrieves extensions from a RingCentral account.

## Endpoint

- **Method:** `GET`
- **Path:** `restapi/v1.0/account/:accountId/extension`
- **Base URL:** `https://platform.ringcentral.com/`
- **Official documentation:** [List Extensions](https://developers.ringcentral.com/api-reference/Extensions/listExtensions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `type` | query | `string` | no |
