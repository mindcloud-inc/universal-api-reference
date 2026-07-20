# Create Conversation with Cliengo

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Create Conversation](https://developers.cliengo.com/reference/conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | body | `string` | yes | The Cliengo company ID that owns the conversation. |
| `websiteId` | body | `string` | yes | The Cliengo website ID where the conversation should be created. |
| `channel` | body | `string` | yes | The conversation channel. Verified working value: WEB. |
| `from` | body | `string` | yes | The visitor identifier for the conversation, such as an email address. |
| `url` | body | `string` | no | Optional source URL associated with the conversation. |
