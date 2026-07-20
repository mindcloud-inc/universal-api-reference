# Search Statements By Registration with GrassBlade LRS

Finds statements in GrassBlade LRS by registration.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Search Statements By Registration](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `registration` | query | `string` | yes | Registration UUID filter. |
