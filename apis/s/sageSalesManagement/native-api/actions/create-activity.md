# Create Activity with Sage Sales Management

Creates an activity in Sage Sales Management.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Create Activity](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Activity date |
| `salesRepId` | body | `number` | yes | Sales representative identifier required by ForceManager when creating an activity. |
| `accountId` | body | `number` | yes | Account identifier required by ForceManager when creating an activity. |
| `typeId` | body | `number` | yes | Activity type identifier required by ForceManager when creating an activity. |
