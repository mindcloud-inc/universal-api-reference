# Create API Key with Confluent

Creates a new API key in Confluent Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v2/api-keys`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Create API Key](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/createIamV2ApiKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `spec.owner.id` | body | `string` | yes |
| `spec.resource.id` | body | `string` | no |
| `spec.display_name` | body | `string` | no |
| `spec.description` | body | `string` | no |
