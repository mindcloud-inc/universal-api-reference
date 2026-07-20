# Search Statements By Time Window with GrassBlade LRS

Finds statements in GrassBlade LRS by time window.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Search Statements By Time Window](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `string` | no | Lower bound stored timestamp filter. |
| `until` | query | `string` | no | Upper bound stored timestamp filter. |
