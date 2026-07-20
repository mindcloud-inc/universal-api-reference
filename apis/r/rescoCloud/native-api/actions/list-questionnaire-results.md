# List Questionnaire Results with Resco Cloud

Retrieves questionnaire results from Resco Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `https://{organization}.rescocrm.com/odata/questionnaires/v4/:template`
- **Base URL:** `https://{organization}.app.resco.net/rest/v1/data`
- **API:** rest
- **Official documentation:** [List Questionnaire Results](https://docs.resco.net/wiki/Questionnaire_OData_service)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | path | `string` | yes | Questionnaire template entity name returned by List Questionnaire Templates. |
| `$select` | query | `string` | no | Comma-separated questionnaire result fields to return. |
| `$expand` | query | `string` | no | OData expand expression for nested questionnaire results. |
| `$filter` | query | `string` | no | OData filter expression. |
