# List Statements with GrassBlade LRS

Retrieves statements from GrassBlade LRS.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [List Statements](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of Statements to return; 0 uses the server maximum. |
