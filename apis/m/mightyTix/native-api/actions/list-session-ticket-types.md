# List Session Ticket Types with Mighty Tix

Retrieves session ticket types from Mighty Tix.

## Endpoint

- **Method:** `POST`
- **Path:** `admin-api/graphql`
- **Base URL:** `https://mindcloudmttix260403.mightytix.com`
- **Official documentation:** [List Session Ticket Types](https://mightytix.com/docs/admin-api#query-sessionTicketTypes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.filter` | body | `object` | no | Optional SessionTicketTypeFilter object from the Mighty Tix Admin GraphQL docs. |
| `variables.paging` | body | `object` | no | Optional CursorPaging object from the Mighty Tix Admin GraphQL docs. |
| `variables.sorting[]` | body | `array<object>` | no | Optional array of SessionTicketTypeSort objects from the Mighty Tix Admin GraphQL docs. |
