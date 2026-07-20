# List Service Accounts with Confluent

Retrieves service accounts from Confluent Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/iam/v2/service-accounts`
- **Base URL:** `https://api.confluent.cloud`
- **Official documentation:** [List Service Accounts](https://docs.confluent.io/cloud/current/api.html#tag/Service-Accounts-(iamv2)/operation/listIamV2ServiceAccounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `display_name` | query | `string` | no | Filter the results by exact match for display_name. |
