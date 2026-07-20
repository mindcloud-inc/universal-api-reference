# Import Contacts in Bulk with Smoove

Imports contacts into Smoove in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Contacts_BulkImport`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Import Contacts in Bulk](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lists_ToSubscribe[]` | body | `array<number>` | no |
| `contacts[]` | body | `array<object>` | yes |
| `overrideNullableValue` | query | `boolean` | no |
| `updateOnlyExistingContacts` | query | `boolean` | no |
