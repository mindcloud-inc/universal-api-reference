# List Answers with Metadata with DataScope Forms

Retrieves submitted answers with metadata from DataScope Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/external/answers`
- **Base URL:** `https://www.mydatascope.com/api`
- **Official documentation:** [List Answers with Metadata](https://dscope.github.io/docs/#get-all-answers-with-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end` | query | `string` | no | End of the date range to fetch answers for. |
| `form_id` | query | `string` | no | Filter answers to a specific DataScope form. |
| `location_id` | query | `string` | no | Filter answers to a specific location. |
| `start` | query | `string` | no | Start of the date range to fetch answers for. |
| `user_id` | query | `string` | no | Filter answers to a specific user. |
