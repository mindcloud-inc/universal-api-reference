# List Locked Rows with Rillion Prime

## Endpoint

- **Method:** `GET`
- **Path:** `/lockedRow`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Locked Rows](https://prime-2-uat-14-ue.rillionprime.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LockedRowID` | query | `number` | no | Optional query value for LockedRowID. |
| `RowType` | query | `number` | no | Optional query value for RowType. |
| `RowID` | query | `number` | no | Optional query value for RowID. |
| `Role` | query | `string` | no | Optional query value for Role. |
| `LoginName` | query | `string` | no | Optional query value for LoginName. |
| `LockedTime` | query | `date` | no | Optional query value for LockedTime. |
