# List Messages with httpSMS

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.httpsms.com/v1`
- **Official documentation:** [List Messages](https://api.httpsms.com/index.html#/Messages/get_messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `owner` | query | `string` | yes | The owner's phone number. |
| `contact` | query | `string` | yes | The contact's phone number. |
| `query` | query | `string` | no | Filter messages containing this query. |
| `limit` | query | `number` | no | Number of messages to return. |
| `skip` | query | `number` | no | Number of messages to skip. |
