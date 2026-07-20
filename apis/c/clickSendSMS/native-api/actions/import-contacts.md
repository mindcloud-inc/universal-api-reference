# Import Contacts with ClickSend SMS

Imports contacts into a ClickSend SMS list.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/lists/:list_id/import`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Import Contacts](https://developers.clicksend.com/docs/contacts/lists/other/create-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `number` | yes | List identifier. |
| `file_url` | body | `string` | yes | Public URL to CSV/XLS/XLSX import file. |
| `field_order[]` | body | `array<string>` | yes | Ordered list of contact field names in the file. |
