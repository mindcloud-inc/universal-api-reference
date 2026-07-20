# Create Viewpoint with Sisense

Creates a new viewpoint in Sisense.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/infusion/viewpoints`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Viewpoint](https://developer.sisense.com/guides/restApi/infusion-api.html#post-infusion-viewpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Unique viewpoint name. |
| `description` | body | `string` | yes | Viewpoint description. |
