# Create Recipient List with Minelead

Creates a recipient list in Minelead.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/recipients/`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [Create Recipient List](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_name` | body | `string` | yes | Name of the recipient list to create. |
| `emails` | body | `list<string>` | yes | Email addresses to include in the recipient list. Send multiple values as a array. |
