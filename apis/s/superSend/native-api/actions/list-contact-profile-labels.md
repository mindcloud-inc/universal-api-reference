# List Contact Profile Labels with SuperSend

Retrieves profile labels for a SuperSend contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/{id}/profile-labels`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [List Contact Profile Labels](https://docs.supersend.io/docs/contact)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
