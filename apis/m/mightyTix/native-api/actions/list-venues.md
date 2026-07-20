# List Venues with Mighty Tix

Retrieves venues from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [List Venues](https://mightytix.com/docs/admin-api#query-venues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.filter` | body | `object` | no | Optional VenueFilter object from the Mighty Tix Admin GraphQL docs. |
| `variables.paging` | body | `object` | no | Optional CursorPaging object from the Mighty Tix Admin GraphQL docs. |
| `variables.sorting[]` | body | `array<object>` | no | Optional array of VenueSort objects from the Mighty Tix Admin GraphQL docs. |
