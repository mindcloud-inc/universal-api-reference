# List People Attributes with Livestorm

Retrieves people attributes from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `people_attributes`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List People Attributes](https://developers.livestorm.co/reference/get_people-attributes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sortable Fields: (-)slug, name, placeholder, created_at, updated_at |
| `filter[builtin]` | query | `string` | no | Filter PeopleAttributes by builtin |
| `filter[description]` | query | `string` | no | Filter PeopleAttributes by description |
| `filter[name]` | query | `string` | no | Filter PeopleAttributes by name |
| `filter[placeholder]` | query | `string` | no | Filter PeopleAttributes by placeholder |
| `filter[slug]` | query | `string` | no | Filter PeopleAttributes by slug |
| `filter[type]` | query | `string` | no | Filter PeopleAttributes by type                       (text, email, avatar, url, consent, unique_select, multiple_select) |
| `filter[user_id]` | query | `string` | no | Filter PeopleAttributes by user_id |
