# Continue Prospect Search with Wiza

Continues a previous prospect search in Wiza.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/continue_search`
- **Base URL:** `https://wiza.co/api`
- **Official documentation:** [Continue Prospect Search](https://docs.wiza.co/api-reference/prospect-lists/continue-prospect-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | ID of the prospect-search list to continue. |
| `max_profiles` | body | `number` | no | Optional number of profiles to return. |
| `callback_url` | body | `string` | no | Optional webhook URL for list updates. |
