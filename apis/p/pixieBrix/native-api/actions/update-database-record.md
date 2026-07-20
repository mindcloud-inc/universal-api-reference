# Update Database Record with PixieBrix

Updates a database record in PixieBrix, creating it if needed.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/databases/:database_pk/records/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Update Database Record](https://docs.pixiebrix.com/developer-api/database-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Updated record data object. |
| `database_pk` | path | `string` | yes | PixieBrix database identifier. |
| `id` | body | `string` | yes | Record id/key to update. |
| `merge_strategy` | body | `string` | no | How PixieBrix should merge record data. Defaults to replace. Accepted values: `0`, `1`, `2`, `3`. |
