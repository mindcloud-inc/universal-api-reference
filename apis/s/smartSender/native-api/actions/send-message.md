# Send Message with Smart Sender

Sends a message to a contact in Smart Sender.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/:contactId/send`
- **Base URL:** `https://api.smartsender.com`
- **Official documentation:** [Send Message](https://smartsendereu.atlassian.net/wiki/spaces/docsru/pages/1676575830/Messages%2BAPI%2B-%2Ben)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Smart Sender contact ID. |
| `content` | body | `string` | yes | Text content for text messages. |
| `type` | body | `string` | yes | The type of message to send. |
