# Add Subscribers to List with SmartrMail

Adds subscribers to a specific SmartrMail list.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/:list_id/list_subscribers`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [Add Subscribers to List](https://docs.smartrmail.com/en/articles/636615-list-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The ID of the requested list. |
| `subscribers` | body | `list<object>` | yes | Array of subscribers to add to the list. |
