# Get Database Asset with PixieBrix

Retrieves a database asset from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/databases/:database_pk/assets/:id/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Database Asset](https://docs.pixiebrix.com/developer-api/database-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database_pk` | path | `string` | yes | PixieBrix database identifier. |
| `id` | path | `string` | yes | PixieBrix database asset identifier. |
