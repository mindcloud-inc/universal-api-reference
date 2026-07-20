# Get Contract with WebWork Time Tracker

Retrieves a contract from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/contracts/:contractId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Get Contract](https://api-docs.webwork-tracker.com/api/contracts/getcontract)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contractId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
