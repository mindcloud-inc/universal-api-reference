# Remove Contact From List with DitLead

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact/{contactId}/remove-from-list`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Remove Contact From List](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Public ID of the contact. |
| `listId` | body | `string` | yes | — |
