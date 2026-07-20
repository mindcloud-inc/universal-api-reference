# Update Recipient List with Minelead

Updates a recipient list in Minelead by adding or removing emails.

## Endpoint

- **Method:** `PUT`
- **Path:** `/campaigns/recipients/`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [Update Recipient List](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Recipient list identifier to update. |
| `operation` | body | `string` | yes | Update operation to apply to the recipient list. |
| `emails` | body | `list<string>` | yes | Email addresses affected by the update operation. Send multiple values as a array. |
