# List Templates with WhatsBox

Retrieves all message templates from WhatsBox.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api.whatsbox.io`
- **Official documentation:** [List Templates](https://api.whatsbox.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter templates by name. |
| `type` | query | `string` | no | Filter templates by type. |
