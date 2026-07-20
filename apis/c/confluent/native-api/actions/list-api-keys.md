# List API Keys with Confluent

Retrieves API keys from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/api-keys`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [List API Keys](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/listIamV2ApiKeys)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `spec.owner` | query | `string` | no |
| `spec.resource` | query | `string` | no |
