# Update API Key with Confluent

Updates an existing API key in Confluent Cloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v2/api-keys/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Update API Key](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/updateIamV2ApiKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `spec.display_name` | body | `string` | no |
| `spec.description` | body | `string` | no |
