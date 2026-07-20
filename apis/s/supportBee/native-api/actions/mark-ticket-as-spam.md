# Mark Ticket as Spam with SupportBee

Marks a SupportBee ticket as spam.

## Endpoint

- **Method:** `POST`
- **Path:** `/tickets/:id/spam`
- **Base URL:** `https://{company}.supportbee.com`
- **Official documentation:** [Mark Ticket as Spam](https://supportbee.com/docs/api/reference#tag/Spam/paths/~1tickets~1{id}~1spam/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | SupportBee ticket ID. |
