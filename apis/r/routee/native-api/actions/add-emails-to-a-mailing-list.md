# Add emails to a mailing list with Routee

Adds emails to a mailing list in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbooks/:id/emails`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Add emails to a mailing list](https://docs.routee.net/reference/adding-emails-to-a-mailing-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | List ID |
| `emails[]` | body | `array<string>` | no | A serialized array of emails |
| `email` | body | `string` | no | The email to be added to the mailing list |
| `variables` | body | `string` | no | The variables to add to the email |
| `phone` | body | `string` | no | To add a phone number, use the system variable Phone |
