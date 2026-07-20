# Create Incoming Message with Missive

Creates an incoming message in your Missive workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Create Incoming Message](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | body | `string` | yes | Account ID from the custom channel settings or Missive Resource IDs. |
| `body` | body | `string` | yes | Incoming message body as HTML or text. |
| `from_field` | body | `object` | yes | Sender object for text or HTML custom channel messages. Include the documented sender fields in the object. |
| `to_fields` | body | `list<object>` | yes | Recipient array for text or HTML custom channel messages. Include the documented recipient objects in the array. |
| `subject` | body | `string` | no | Subject line for email messages only. |
