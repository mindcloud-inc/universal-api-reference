# Remove Subscriber From List with SmartrMail

Removes a subscriber from a specific SmartrMail list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/lists/:list_id/list_subscribers/:email_or_phone_or_uid`
- **Base URL:** `https://go.smartrmail.com/api/v1`
- **Official documentation:** [Remove Subscriber From List](https://docs.smartrmail.com/en/articles/636615-list-subscribers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_or_phone_or_uid` | path | `string` | yes | The email address, phone number, or UID of the requested subscriber. |
| `list_id` | path | `string` | yes | The ID of the requested list. |
