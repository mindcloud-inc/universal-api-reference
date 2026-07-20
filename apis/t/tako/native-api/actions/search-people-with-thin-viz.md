# Search People with Thin-Viz with Tako

Searches people with Thin-Viz in Tako.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/thin_viz/search_people/`
- **Base URL:** `https://tako.com/api`
- **Official documentation:** [Search People with Thin-Viz](https://docs.tako.com/api-reference/thinviz-search-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Person name, optionally with company or role context. |
