# Rename translation memory with Lara Translate

Updates an existing translation memory in Lara Translate.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://mcp-v2.laratranslate.com/v1`
- **Official documentation:** [Rename translation memory](https://developers.laratranslate.com/docs/manage-translation-memories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | ID of the translation memory to rename. |
| `name` | body | `string` | yes | New name for the translation memory. |
