# List Certificates with Paradym

Retrieves a list of certificates from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/certificates`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List Certificates](https://paradym.id/reference#tag/certificates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[type]` | query | `string` | no | Filter certificates by Paradym certificate type. Accepted values: `0`, `1`. |
| `filter[keyType]` | query | `string` | no | Filter certificates by key type. Accepted values: `0`, `1`. |
| `filter[status]` | query | `string` | no | Filter certificates by certificate status. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
