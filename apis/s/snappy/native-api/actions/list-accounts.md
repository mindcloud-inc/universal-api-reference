# List Accounts with Snappy

Retrieves accounts from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [List Accounts](https://docs.snappy.com/reference/getaccounts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | query | `string` | no | Company ID. |
| `name` | query | `string` | no | The name of the account. |
| `fields[]` | query | `array<string>` | no | Additional account fields to include. |
| `skip` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return per page. |
