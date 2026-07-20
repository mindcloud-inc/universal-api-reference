# List Sessions with Mighty Tix

Retrieves sessions from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [List Sessions](https://mightytix.com/docs/admin-api#query-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.filter` | body | `object` | no | Optional SessionFilter object from the Mighty Tix Admin GraphQL docs. |
| `variables.paging` | body | `object` | no | Optional CursorPaging object from the Mighty Tix Admin GraphQL docs. |
| `variables.sorting[]` | body | `array<object>` | no | Optional array of SessionSort objects from the Mighty Tix Admin GraphQL docs. |
