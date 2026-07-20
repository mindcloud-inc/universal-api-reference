# Get Estimate with FreshBooks

Retrieves an estimate from FreshBooks for an account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/account/:accountId/estimates/estimates/:estimateId`
- **Base URL:** `https://api.freshbooks.com`
- **Official documentation:** [Get Estimate](https://www.freshbooks.com/api/estimates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | FreshBooks accounting account ID. |
| `estimateId` | path | `string` | yes | FreshBooks estimate ID. |
