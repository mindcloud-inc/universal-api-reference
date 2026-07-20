# Get Message Status with Callbell

Retrieves message status details from Callbell.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/status/:uuid`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Get Message Status](https://docs.callbell.eu/api/reference/messages_api/get_message_status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Identifier of the message sent through the API. |
