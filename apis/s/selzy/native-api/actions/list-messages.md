# List Messages with Selzy

Retrieves messages from Selzy.

## Endpoint

- **Method:** `POST`
- **Path:** `getMessages`
- **Base URL:** `https://api.selzy.com/en/api`
- **Official documentation:** [List Messages](https://selzy.com/en/support/api/statistics/getmessages/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | yes | Lower UTC bound for message creation time in YYYY-MM-DD hh:mm format. |
| `date_to` | query | `string` | yes | Upper UTC bound for message creation time in YYYY-MM-DD hh:mm format. |
| `limit` | query | `number` | no | Maximum number of messages to return, from 1 to 100. |
| `offset` | query | `number` | no | Zero-based starting position for the result set. |
