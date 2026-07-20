# Read Service Account with Confluent

Retrieves a service account from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/service-accounts/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Read Service Account](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/getIamV2ServiceAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier for the service account. |
