# Create Contact Note with Cliengo

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/notes`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Create Contact Note](https://developers.cliengo.com/reference/contactcontactidnotes-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Identifier of the Cliengo contact. |
| `message` | body | `string` | yes | Text note. |
