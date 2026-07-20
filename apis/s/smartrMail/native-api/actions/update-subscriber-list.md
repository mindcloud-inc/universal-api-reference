# Update Subscriber List with SmartrMail

Updates an existing subscriber list in SmartrMail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:list_id`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [Update Subscriber List](https://docs.smartrmail.com/en/articles/636612-manage-subscriber-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the requested list. |
| `name` | body | `string` | yes | The updated name of the subscriber list. |
