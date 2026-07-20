# Get Message Status with Sendblue

Retrieves the status of a message from Sendblue.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/status`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Get Message Status](https://docs.sendblue.com/api/resources/messages/methods/get_status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | query | `string` | yes | Message handle returned by Sendblue when the message was created. |
