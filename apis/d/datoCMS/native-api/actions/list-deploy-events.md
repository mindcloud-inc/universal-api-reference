# List Deploy Events with DatoCMS

## Endpoint

- **Method:** `GET`
- **Path:** `/build-events`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [List Deploy Events](https://www.datocms.com/docs/content-management-api/resources/build-event/instances)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[ids]` | query | `string` | no | Comma-separated deploy event IDs to return. Send multiple values as a array. |
| `filter[fields][event_type][eq]` | query | `string` | no | Filter deploy events by event type. |
| `filter[fields][build_trigger_id][eq]` | query | `string` | no | Filter deploy events by build trigger ID. |
| `filter[fields][created_at][gt]` | query | `date` | no | Include events created after this timestamp (ISO-8601). |
| `filter[fields][created_at][lt]` | query | `date` | no | Include events created before this timestamp (ISO-8601). |
| `order_by` | query | `string` | no | Sort expression such as created_at_desc or event_type_asc. |
