# List Affiliates with GoAffPro

Retrieves a list of affiliates from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/affiliates`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Affiliates](https://api.goaffpro.com/docs/admin/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Only return affiliates matching this email address. |
| `fields[]` | query | `array<string>` | yes | Fields to include in the returned affiliate records. |
| `status` | query | `string` | no | Only return affiliates with this status. |
