# List Activities with Helpjuice

Retrieves activities from Helpjuice.

## Endpoint

- **Method:** `GET`
- **Path:** `/activities`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List Activities](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action_type` | query | `string` | no | Filter activities by the action performed, such as create or update. |
| `chronologically` | query | `boolean` | no | Return activities ordered from oldest to newest. |
| `filter[owner_id]` | query | `number` | no | Filter activities by the user who performed them. |
| `older_than` | query | `number` | no | Filter activities that happened before the specified activity id. |
| `reverse_chronologically` | query | `boolean` | no | Return activities ordered from newest to oldest. |
| `trackable_id` | query | `number` | no | Filter activities for a specific Helpjuice item id. |
| `trackable_type` | query | `string` | no | Filter activities by Helpjuice trackable type such as Question or Category. |
