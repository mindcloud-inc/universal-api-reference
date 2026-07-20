# List Answers with DataScope Forms

Retrieves submitted answers from DataScope Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/external/v2/answers`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [List Answers](https://dscope.github.io/docs/#get-all-answers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | query | `number` | no | Filter answers to a specific DataScope form. |
| `user_id` | query | `string` | no | Filter answers to a specific user. |
| `start` | query | `string` | no | Start of the date range to fetch answers for. |
| `end` | query | `string` | no | End of the date range to fetch answers for. |
| `location_id` | query | `number` | no | Filter answers to a specific location. |
| `date_modified` | query | `boolean` | no | Use the answer modification date instead of the creation date when filtering. |
