# Search Messages by Email Message ID with Missive

Finds Missive messages by email message ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Search Messages by Email Message ID](https://missiveapp.com/docs/developers/rest-api/endpoints#list-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_message_id` | query | `string` | yes | Email Message-ID header value. |
