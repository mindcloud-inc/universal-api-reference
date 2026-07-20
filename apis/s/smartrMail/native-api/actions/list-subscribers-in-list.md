# List Subscribers in List with SmartrMail

Retrieves subscribers from a specific SmartrMail list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:list_id/list_subscribers`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [List Subscribers in List](https://docs.smartrmail.com/en/articles/636615-list-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the requested list. |
