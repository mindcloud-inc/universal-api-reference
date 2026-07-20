# Search in Application v2 with Podio

Finds results in a Podio application.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/app/:app_id/v2`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [Search in Application v2](https://developers.podio.com/doc/search/search-in-application-v2-155196220)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | The ID of the application to search. |
| `query` | query | `string` | no | The text to search for. |
| `ref_type` | query | `list<string>` | no | Restrict the search to a specific object type. Accepted values: `app`, `conversation`, `file`, `item`, `profile`, `status`, `task`. |
| `counts` | query | `boolean` | no | Return counts for each result type. |
| `highlights` | query | `boolean` | no | Return highlighted matches for each result. |
| `search_fields[]` | query | `array<string>` | no | The list of fields to search in. |
