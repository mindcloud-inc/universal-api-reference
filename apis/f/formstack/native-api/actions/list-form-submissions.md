# List Form Submissions with Formstack

Retrieves submissions for a form from Formstack.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/submissions`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [List Form Submissions](https://developers.formstack.com/reference/getformsubmissionslist-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The unique identifier of the form to retrieve submissions from. |
| `keyword` | query | `string` | no | Search term to filter submissions by content across all fields. |
| `order` | query | `list<string>` | no | Sort order for results (ASC or DESC). Accepted values: `ASC`, `DESC`. |
| `minTime` | query | `date` | no | Return submissions created on or after this date/time. |
| `maxTime` | query | `date` | no | Return submissions created on or before this date/time. |
| `search[]` | query | `array<object>` | no | Array of search criteria to filter submissions by specific field values. |
| `search[].fieldId` | query | `string` | no | The ID of the field to search. |
| `search[].value` | query | `string` | no | The value to search for in the field. |
| `data` | query | `list<string>` | no | Include field data in the response (true/false). Accepted values: `false`, `true`. |
| `expandData` | query | `list<string>` | no | Include expanded field data with parsed values (true/false). Accepted values: `false`, `true`. |
| `prettyName` | query | `list<string>` | no | Include a human-readable name for each submission (true/false). Accepted values: `false`, `true`. |
