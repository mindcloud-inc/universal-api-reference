# Upsert Records with Zoho Recruit

Inserts or updates records in a Zoho Recruit module.

## Endpoint

- **Method:** `POST`
- **Path:** `/:moduleApiName/upsert`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Upsert Records](https://www.zoho.com/recruit/developer-guide/apiv2/upsert-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleApiName` | path | `string` | yes | The Zoho Recruit module API name where the records should be upserted. |
| `data` | body | `list<object>` | yes | An array of record objects to upsert. |
| `duplicate_check_fields` | body | `list<string>` | no | Field API names to use for duplicate matching during upsert. |
| `trigger` | body | `list<string>` | no | Automation triggers to run after the upsert. |
