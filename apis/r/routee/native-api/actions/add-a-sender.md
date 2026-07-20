# Add a sender with Routee

Adds a new sender in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/senders`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Add a sender](https://docs.routee.net/reference/adding-a-sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | the email to be added as sender |
| `name` | body | `string` | no | Name of the email |
