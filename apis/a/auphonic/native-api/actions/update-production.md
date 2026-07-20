# Update Production with Auphonic

Updates an existing production in Auphonic.

## Endpoint

- **Method:** `POST`
- **Path:** `/production/:uuid.json`
- **Base URL:** `https://auphonic.com/api`
- **Official documentation:** [Update Production](https://auphonic.com/help/api/update.html#update-a-production-or-preset-and-reset-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID of the production. |
| `output_basename` | body | `string` | no | Updated basename for generated output files. |
| `reset_data` | body | `boolean` | no | Clear the existing mutable production data before applying the update. |
