# List Issued Credentials with Paradym

Retrieves issued credentials from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/issuance`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List Issued Credentials](https://paradym.id/reference#tag/issued-credentials)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter[credentialTemplateId]` | query | `string` | no |
| `filter[status]` | query | `string` | no |
| `filter[exchange]` | query | `string` | no |
