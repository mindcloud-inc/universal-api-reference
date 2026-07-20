# Create Note with QuickFile

## Endpoint

- **Method:** `POST`
- **Path:** `/system/createnote`
- **Base URL:** `https://api.quickfile.co.uk/1_2`
- **Official documentation:** [Create Note](https://api.quickfile.co.uk/d/v1_2/System_CreateNote)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Note` | body | `string` | yes | Note body to attach in QuickFile. |
| `PostedBy` | body | `string` | no | Display name to attribute on the note. |
| `ClientID` | body | `number` | no | Client record to attach the note to. |
| `SupplierID` | body | `number` | no | Supplier record to attach the note to. |
| `InvoiceID` | body | `number` | no | Invoice record to attach the note to. |
| `PurchaseID` | body | `number` | no | Purchase record to attach the note to. |
