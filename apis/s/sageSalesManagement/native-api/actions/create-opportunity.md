# Create Opportunity with Sage Sales Management

Creates an opportunity in Sage Sales Management.

## Endpoint

- **Method:** `POST`
- **Path:** `/opportunities`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Create Opportunity](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesRepId` | body | `string` | yes | Sales representative ID |
| `salesProbability` | body | `number` | yes | Opportunity sales probability required by ForceManager when creating an opportunity. |
| `reference` | body | `string` | yes | Opportunity reference required by ForceManager when creating an opportunity. |
| `statusId` | body | `number` | yes | Opportunity status identifier required by ForceManager when creating an opportunity. |
| `branchId` | body | `number` | yes | Branch identifier required by ForceManager when creating an opportunity. |
