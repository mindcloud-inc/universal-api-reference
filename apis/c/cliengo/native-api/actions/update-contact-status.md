# Update Contact Status with Cliengo

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactId/status`
- **Base URL:** `https://api.cliengo.com/1.0`
- **Official documentation:** [Update Contact Status](https://developers.cliengo.com/reference/contactscontactidstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Identifier of the Cliengo contact. |
| `externalStatus` | body | `string` | yes | New contact status. Possible values include NEW, ACTIVE, LONG_TERM, and CLIENT. |
