# List Secrets with Devin

Retrieves a list of secrets from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/secrets`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [List Secrets](https://docs.devin.ai/api-reference/v3/secrets/organizations-secrets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
