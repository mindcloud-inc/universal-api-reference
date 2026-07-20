# Search Contacts with CalendarHero

Finds contacts in CalendarHero by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact`
- **Base URL:** `https://api.calendarhero.com`
- **Official documentation:** [Search Contacts](https://api.calendarhero.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `all` | query | `string` | no | Include all matching contacts. |
| `filter` | query | `string` | no | Filter expression for contacts. |
| `includeTeams` | query | `string` | no | Include team contacts in the search. |
| `search` | query | `string` | no | Search text for matching contacts. |
