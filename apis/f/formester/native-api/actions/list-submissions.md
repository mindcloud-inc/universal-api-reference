# List Submissions with Formester

Retrieves submissions from Formester.

## Endpoint

- **Method:** `GET`
- **Path:** `/submissions`
- **Base URL:** `https://app.formester.com/api/v2`
- **Official documentation:** [List Submissions](https://docs.formester.com/formester-api-v2#list-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_uuid` | query | `string` | no | Recommended form identifier. |
| `form_id` | query | `number` | no | Numeric form identifier. |
| `sort` | query | `string` | no | — |
| `order` | query | `list<string>` | no | Accepted values: `asc`, `desc`. |
