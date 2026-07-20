# Create document with Atlar

Creates a document in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounting/v2beta/documents`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create document](https://docs.atlar.com/reference/post-accounting-v2beta-documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `glEntityId` | body | `string<string>` | yes |
| `type` | body | `string<string>` | yes |
| `amount` | body | `object<string>` | yes |
| `date` | body | `date<string>` | yes |
| `description` | body | `string<string>` | yes |
| `references` | body | `object<string>` | yes |
| `voided` | body | `boolean<string>` | yes |
| `reconciliationStatus` | body | `string<string>` | yes |
| `glEntries[]` | body | `array<object>` | yes |
| `provenance` | body | `object<string>` | yes |
| `vendorCreated` | body | `date<string>` | yes |
