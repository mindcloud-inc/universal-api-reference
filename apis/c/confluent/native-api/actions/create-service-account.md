# Create Service Account with Confluent

Creates a new service account in Confluent Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v2/service-accounts`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Create Service Account](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/createIamV2ServiceAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_name` | body | `string` | yes | The name of the service account. |
| `description` | body | `string` | no | A description of how this service account is used. |
| `assigned_resource_owner` | query | `string` | no | The resource_id of the principal who will be assigned resource owner on the created service account. |
