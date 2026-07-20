# Delete Subscriber with MailerLite

Deletes a subscriber from MailerLite while keeping their information.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/subscribers/:id`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Delete Subscriber](https://developers.mailerlite.com/docs/subscribers#delete-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Subscriber ID for the account. |
