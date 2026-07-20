# List Events with Mighty Tix

Retrieves events from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [List Events](https://mightytix.com/docs/admin-api#query-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.filter` | body | `object` | no | Optional EventFilter object from the Mighty Tix Admin GraphQL docs. |
| `variables.paging` | body | `object` | no | Optional CursorPaging object from the Mighty Tix Admin GraphQL docs. |
| `variables.sorting[]` | body | `array<object>` | no | Optional array of EventSort objects from the Mighty Tix Admin GraphQL docs. |
