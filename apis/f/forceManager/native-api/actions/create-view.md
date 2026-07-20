# Create View with ForceManager

Creates a new view in ForceManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/views`
- **Official documentation:** [Create View](https://support.forcemanager.net/en/articles/8613478-entity-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the view. |
| `entity` | body | `string` | yes | Entity where the view filter was applied. |
