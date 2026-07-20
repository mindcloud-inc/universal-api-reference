# List Contact Persons with Megaventory

Retrieves contact person records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ContactPersonGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Contact Persons](https://api.megaventory.com/v2017a/json/metadata?op=ContactPersonGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `showDeleted` | body | `boolean` | no | Include archived contact person records. |
