# Get Registry Brick with PixieBrix

Retrieves a brick package from the PixieBrix registry.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/registry/bricks/:name/`
- **Base URL:** `https://app.pixiebrix.com`
- **Official documentation:** [Get Registry Brick](https://docs.pixiebrix.com/developer-api/package-management-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kind` | query | `string` | no | Registry brick kind filter. |
| `name` | path | `string` | yes | PixieBrix registry package name. |
