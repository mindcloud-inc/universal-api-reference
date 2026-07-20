# Search Apps with Shuffler

Finds apps in Shuffler by search query.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/search`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Search Apps](https://shuffler.io/docs/API#search-existing-apps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | body | `string` | yes | App search string. |
