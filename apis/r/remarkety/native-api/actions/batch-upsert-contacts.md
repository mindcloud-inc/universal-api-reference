# Batch Upsert Contacts with Remarkety

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/stores/{storeId}/contacts/batch`
- **Base URL:** `https://app.remarkety.com`
- **Official documentation:** [Batch Upsert Contacts](https://support.remarkety.com/hc/en-us/articles/360000694746-Uploading-contacts-in-batch-via-API)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes |
| `update_existing` | body | `boolean` | no |
| `append_tags` | body | `boolean` | no |
