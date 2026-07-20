# Receive the activation code at the sender’s email address with Routee

Sends an activation code to the sender email in Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/senders/:email/code`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Receive the activation code at the sender’s email address](https://docs.routee.net/reference/receiving-the-activation-code-at-the-senders-email-address)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | the email to sent the activation code |
