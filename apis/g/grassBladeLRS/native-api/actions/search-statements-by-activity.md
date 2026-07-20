# Search Statements By Activity with GrassBlade LRS

Finds statements in GrassBlade LRS by activity.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Search Statements By Activity](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activity` | query | `string` | yes | Activity ID filter. |
