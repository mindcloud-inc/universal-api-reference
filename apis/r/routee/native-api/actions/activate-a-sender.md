# Activate a sender with Routee

Activates an existing sender in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/senders/:email/code`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Activate a sender](https://docs.routee.net/reference/activating-a-sender)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | the email to sent the activation code |
| `code` | body | `string` | yes | the code |
