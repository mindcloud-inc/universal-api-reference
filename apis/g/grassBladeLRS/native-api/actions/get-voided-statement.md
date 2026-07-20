# Get Voided Statement with GrassBlade LRS

Retrieves a voided statement from GrassBlade LRS.

## Endpoint

- **Method:** `GET`
- **Path:** `/statements`
- **Base URL:** `https://test.gblrs.com/xAPI`
- **Official documentation:** [Get Voided Statement](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voidedStatementId` | query | `string` | no | ID of voided Statement to fetch. |
