# Delete Service Account with Confluent

Deletes an existing service account from Confluent Cloud.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/iam/v2/service-accounts/:id`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [Delete Service Account](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/deleteIamV2ServiceAccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier for the service account. |
