# List Ticket Types with Mighty Tix

Retrieves ticket types from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [List Ticket Types](https://mightytix.com/docs/admin-api#query-ticketTypes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.filter` | body | `object` | no | Optional TicketTypeFilter object from the Mighty Tix Admin GraphQL docs. |
| `variables.paging` | body | `object` | no | Optional CursorPaging object from the Mighty Tix Admin GraphQL docs. |
| `variables.sorting[]` | body | `array<object>` | no | Optional array of TicketTypeSort objects from the Mighty Tix Admin GraphQL docs. |
