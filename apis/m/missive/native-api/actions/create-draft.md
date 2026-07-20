# Create Draft with Missive

Creates a draft in your Missive workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/drafts`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Create Draft](https://missiveapp.com/docs/developers/rest-api/endpoints#create-a-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | no | Draft subject. |
| `body` | body | `string` | no | Draft body as HTML or text. |
| `conversation` | body | `string` | no | Conversation ID to append the draft to an existing conversation. |
