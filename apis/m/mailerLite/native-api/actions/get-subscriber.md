# Get Subscriber with MailerLite

Retrieves a subscriber from MailerLite by ID or email.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscribers/:idOrEmail`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [Get Subscriber](https://developers.mailerlite.com/docs/subscribers#fetch-a-subscriber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrEmail` | path | `string` | yes | Subscriber ID or email address to fetch. |
