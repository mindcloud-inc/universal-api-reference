# Create Table with Airtable

Creates a new table in a specific Airtable base.

## Endpoint

- **Method:** `POST`
- **Path:** `/meta/bases/:baseId/tables`
- **Base URL:** `https://api.airtable.com/v0`
- **Official documentation:** [Create Table](https://airtable.com/developers/web/api/create-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `list<string>` | yes | — |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `fields[]` | body | `array<object>` | yes | — |
| `fields[].name` | body | `string` | yes | — |
| `fields[].type` | body | `list<string>` | yes | Accepted values: `aiText`, `autoNumber`, `barcode`, `button`, `checkbox`, `count`, `createdBy`, `createdTime`, `currency`, `date`, `dateTime`, `duration`, `email`, `externalSyncSource`, `formula`, `lastModifiedBy`, `lastModifiedTime`, `lookup`, `multilineText`, `multipleAttachments`, `multipleCollaborators`, `multipleRecordLinks`, `multipleSelects`, `number`, `percent`, `phoneNumber`, `rating`, `richText`, `rollup`, `singleCollaborator`, `singleLineText`, `singleSelect`, `url`. |
| `fields[].description` | body | `string` | no | — |
| `fields[].options` | body | `object` | no | — |
