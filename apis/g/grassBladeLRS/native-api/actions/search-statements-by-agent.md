# Search Statements By Agent with GrassBlade LRS

Finds statements in GrassBlade LRS by agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Search Statements By Agent](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent` | query | `string` | yes | Agent or identified group JSON filter. |
