# Create translation memory with Lara Translate

Creates a new translation memory in Lara Translate.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://mcp-v2.laratranslate.com/v1`
- **Official documentation:** [Create translation memory](https://developers.laratranslate.com/docs/manage-translation-memories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the translation memory to create. |
| `external_id` | body | `string` | no | Optional MyMemory import identifier in the form ext_my_[id]. |
