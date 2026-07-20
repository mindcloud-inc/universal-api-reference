# Forget Subscriber with MailerLite

Deletes a subscriber from MailerLite and permanently removes their data.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscribers/:id/forget`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Forget Subscriber](https://developers.mailerlite.com/docs/subscribers#forget-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Subscriber ID for the account. |
