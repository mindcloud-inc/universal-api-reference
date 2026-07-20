# Unsubscribe Subscriber with Sequenzy

Unsubscribes an existing subscriber in Sequenzy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/subscribers/:email`
- **Base URL:** `https://api.sequenzy.com/api/v1`
- **Official documentation:** [Unsubscribe Subscriber](https://docs.sequenzy.com/api-reference/subscribers/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Subscriber email address. |
