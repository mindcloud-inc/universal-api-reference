# List Roles with Seqera

Retrieves available roles from Seqera.

## Endpoint

- **Method:** `GET`
- **Path:** `/roles`
- **Base URL:** `https://api.cloud.seqera.io`
- **Official documentation:** [List Roles](https://cloud.seqera.io/openapi/seqera-api-latest.yml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | query | `number` | yes | — |
| `max` | query | `number` | no | Maximum number of roles to return. |
| `offset` | query | `number` | no | Number of roles to skip before returning results. |
