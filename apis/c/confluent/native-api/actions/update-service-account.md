# Update Service Account with Confluent

Updates an existing service account in Confluent Cloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v2/service-accounts/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Update Service Account](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/updateIamV2ServiceAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier for the service account. |
| `display_name` | body | `string` | no | The name of the service account. |
| `description` | body | `string` | no | A description of how this service account is used. |
