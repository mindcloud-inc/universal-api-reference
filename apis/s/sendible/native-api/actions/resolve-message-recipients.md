# Resolve Message Recipients with Sendible

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.prd-tw.sendible.com/v1.0/messages/{{messageId}}/resolve`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [Resolve Message Recipients](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The Sendible message ID. |
| `recipientIds` | body | `list<number>` | yes | Recipient IDs to resolve. |
