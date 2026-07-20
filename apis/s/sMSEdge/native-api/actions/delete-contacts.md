# Delete Contacts with SMSEdge

Deletes contacts from a SMSEdge list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/numbers/delete/`
- **Base URL:** `https://api.smsedge.com/v1`
- **Official documentation:** [Delete Contacts](https://developers.smsedge.io/reference/numbers-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-separated IDs of numbers to be deleted |
