# Get Database with PixieBrix

Retrieves a database from PixieBrix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/organizations/:organization_pk/databases/:id/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Database](https://docs.pixiebrix.com/developer-api/database-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | PixieBrix database identifier. |
| `organization_pk` | path | `string` | yes | PixieBrix organization identifier. |
