# Create Prospect List with Wiza

Creates a Wiza prospect list from filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospects/create_prospect_list`
- **Base URL:** `https://wiza.co/api`
- **Official documentation:** [Create Prospect List](https://docs.wiza.co/api-reference/prospect-lists/create-prospect-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | yes | Prospect list filter object. |
| `list` | body | `object` | yes | List settings object including name and max_profiles. |
