# Create Database Record with PixieBrix

Creates a database record in PixieBrix, merging by key if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/databases/:database_pk/records/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Create Database Record](https://docs.pixiebrix.com/developer-api/database-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Record data object. |
| `database_pk` | path | `string` | yes | PixieBrix database identifier. |
| `id` | body | `string` | yes | Record id/key to create. |
| `merge_strategy` | body | `string` | no | How PixieBrix should merge record data. Defaults to replace. Accepted values: `0`, `1`, `2`, `3`. |
