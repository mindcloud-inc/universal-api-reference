# List Messages by WhatsApp Number with Wati

Retrieves message history for a WhatsApp number from Wati.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/getMessages/:whatsappNumber`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [List Messages by WhatsApp Number](https://docs.wati.io/reference/get_api-v1-getmessages-whatsappnumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | path | `string` | yes | WhatsApp phone number whose messages should be retrieved. |
| `pageSize` | query | `number` | no | Number of messages to return per page. |
| `pageNumber` | query | `number` | no | Page number to return. |
