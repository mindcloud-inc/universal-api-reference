# Search Constituents with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `constituent/v1/constituents/search`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [Search Constituents](https://developer.blackbaud.com/skyapi/renxt/constituent/entities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_text` | query | `string` | yes | Text to search across constituent records. |
| `include_inactive` | query | `boolean` | no | Include inactive constituents in the search results. |
| `search_field` | query | `string` | no | Optional field to target when running the search. |
