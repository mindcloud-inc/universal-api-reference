# Read API Key with Confluent

Retrieves an API key from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/api-keys/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Read API Key](https://docs.confluent.io/cloud/current/api.html#tag/API-Keys-(iamv2)/operation/getIamV2ApiKey)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
