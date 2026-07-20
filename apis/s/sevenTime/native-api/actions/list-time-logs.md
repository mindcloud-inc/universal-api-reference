# List Time Logs with Seven Time

Retrieves time logs from a Seven Time workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/timeLogs`
- **Base URL:** `https://app.seventime.se/api/2`
- **Official documentation:** [List Time Logs](https://docs.seventime.se/#get-time-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | query | `string` | no | Filter time logs by user id. |
| `customer` | query | `string` | no | Filter time logs by customer id. |
| `project` | query | `string` | no | Filter time logs by project id. |
| `task` | query | `string` | no | Filter time logs by task id. |
| `category` | query | `string` | no | Filter time logs by category id. |
| `workOrder` | query | `string` | no | Filter time logs by work order id. |
| `workOrderNumber` | query | `string` | no | Filter time logs by work order number. |
| `timestamp` | query | `date` | no | Include time logs that start after the given timestamp. |
| `endTimestamp` | query | `date` | no | Include time logs that end before the given timestamp. |
| `invoicedDate` | query | `date` | no | Include time logs invoiced since the given timestamp. |
| `isAbsence` | query | `boolean` | no | Filter time logs by absence status. |
| `lastModified` | query | `date` | no | Include time logs modified since the given timestamp. |
