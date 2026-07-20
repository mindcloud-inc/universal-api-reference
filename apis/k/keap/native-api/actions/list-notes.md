# List Notes with Keap

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contact_id/notes`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [List Notes](https://developer.keap.com/docs/restv2/#tag/Note/operation/listNotes)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier of the contact. |
