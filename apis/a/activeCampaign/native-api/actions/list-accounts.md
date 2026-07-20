# List Accounts with ActiveCampaign

Retrieves accounts from ActiveCampaign.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `{apiUrl}/api/3`
- **Official documentation:** [List Accounts](https://developers.activecampaign.com/reference/list-all-accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count_deals` | query | `string` | no | Whether to compute associated contact/deal counts. |
| `search` | query | `string` | no | Search by account name. |
