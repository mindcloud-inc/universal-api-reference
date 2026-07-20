# Start WhatsApp Conversation with WotNot

Creates a WhatsApp conversation in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversations`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Start WhatsApp Conversation](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Configured WhatsApp sender number |
| `to.phone` | body | `string` | yes | Recipient phone number |
| `to.name` | body | `string` | no | Recipient display name |
| `to.email` | body | `string` | no | Recipient email |
| `message.data.template` | body | `string` | yes | Approved WhatsApp template name |
| `assignee` | body | `string` | yes | Assigned agent email |
