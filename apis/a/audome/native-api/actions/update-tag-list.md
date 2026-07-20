# Update Tag List with Audome

Updates an existing tag list in Audome.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tag-lists/:taglistUuid`
- **Base URL:** `https://app.audome.com/api/v1`
- **Official documentation:** [Update Tag List](https://app.audome.com/api-documentation#endpoints-PATCHapi-v1-tag-lists--taglistUuid-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Updated name for the tag list. |
| `taglistUuid` | path | `string` | yes | Numeric tag-list identifier. |
