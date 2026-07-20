# Unsubscribing a recipient with Routee

Unsubscribes a recipient from Routee email delivery.

## Endpoint

- **Method:** `POST`
- **Path:** `/smtp/unsubscribe`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Unsubscribing a recipient](https://docs.routee.net/reference/unsubscribing-a-recipient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails` | body | `string` | no | A serialized email array |
