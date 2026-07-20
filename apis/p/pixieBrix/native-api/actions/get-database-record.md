# Get Database Record with PixieBrix

Retrieves a record from a PixieBrix database.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/databases/:database_pk/records/:key/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Database Record](https://docs.pixiebrix.com/developer-api/database-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_pk` | path | `string` | yes | PixieBrix database identifier. |
| `key` | path | `string` | yes | PixieBrix database record key. |
