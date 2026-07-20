# Update Contact Person with Megaventory

Updates a contact person in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ContactPersonUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Contact Person](https://api.megaventory.com/v2017a/json/metadata?op=ContactPersonUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvContactPerson` | body | `object` | yes | Contact person payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
