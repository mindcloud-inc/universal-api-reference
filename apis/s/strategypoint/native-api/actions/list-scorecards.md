# List Scorecards with Strategypoint

Retrieves scorecards from Strategypoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/scorecards`
- **Base URL:** `https://app.clearpointstrategy.com/api/v1`
- **Official documentation:** [List Scorecards](https://developer.clearpointstrategy.com/reference/listscorecards-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `count` | query | `number` | no | Count per page. |
| `include` | query | `string` | no | Include deleted or menu data. |
| `userId` | query | `number` | no | Limit the results to one user. |
| `periodId` | query | `number` | no | Reporting period ID. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
