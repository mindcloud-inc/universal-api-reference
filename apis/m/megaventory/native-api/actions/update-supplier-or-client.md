# Update Supplier or Client with Megaventory

Updates a supplier or client in Megaventory using a record action.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SupplierClientUpdate`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [Update Supplier or Client](https://api.megaventory.com/v2017a/json/metadata?op=SupplierClientUpdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mvSupplierClient` | body | `object` | yes | Supplier or client payload to insert, update, or delete. |
| `mvRecordAction` | body | `string` | yes | Megaventory record action such as Insert, Update, or Delete. |
| `mvGrantPermissionsToAllUsers` | body | `boolean` | no | Grant created record permissions to all users. |
| `mvInsertUpdateDeleteSourceApplication` | body | `string` | no | Source application label Megaventory should store for the change. |
