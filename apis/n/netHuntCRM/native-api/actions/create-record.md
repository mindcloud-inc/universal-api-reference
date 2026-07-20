# Create Record with NetHunt CRM

Creates a new record in NetHunt CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/create-record/:folderId`
- **Base URL:** `https://nethunt.com/api/v1/zapier`
- **Official documentation:** [Create Record](https://nethunt.com/integration-api#create-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `object` | yes | Record fields payload keyed by NetHunt field name. |
| `folderId` | path | `string` | yes | Folder ID to create the record in. |
| `timeZone` | body | `string` | yes | User time zone used when creating the record. |
