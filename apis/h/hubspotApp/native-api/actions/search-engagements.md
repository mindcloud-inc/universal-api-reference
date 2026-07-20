# Search Engagements with HubSpot

Finds engagement records in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/:engagementType/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Engagements](https://developers.hubspot.com/docs/api-reference/crm-objects-v3/search/post-crm-v3-objects-objectType-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `engagementType` | path | `list` | yes | The CRM activity object type to search, such as notes, tasks, calls, emails, or meetings. Accepted values: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. |
| `filterGroups` | body | `object<object>` | no | Use HubSpot filter groups to find activities linked to a record. For deal activity, use `associations.deal` with `EQ` and the deal ID. You can also use `associations.contact` or `associations.company`. |
| `filterGroups[].filters[]` | body | `array<object>` | no | Filters combined with AND semantics inside one filter group. For deal activity, add a filter using `associations.deal` and the deal ID. |
| `filterGroups[].filters[].propertyName` | body | `string` | no | HubSpot property to filter on. For related-record activity lookups, use `associations.deal`, `associations.contact`, or `associations.company`. |
| `filterGroups[].filters[].operator` | body | `list<string>` | no | Comparison operator for the filter. `EQ` is the usual choice for association filters such as `associations.deal = <dealId>`. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | Single comparison value for the filter. For deal activity lookups, pass the deal ID such as `9018868490`. |
| `properties[]` | body | `array<string>` | no | Properties to return for each activity. For deal emails, try `hs_email_subject`, `hs_email_text`, `hs_email_from_email`, `hs_email_to_email`, and `hs_timestamp`. For deal notes, try `hs_note_body` and `hs_timestamp`. |
| `query` | body | `string` | no | Optional full-text query applied to the default searchable properties for the selected activity type. |
| `limit` | body | `number` | no | Maximum number of records to return in this search page. |
| `after` | body | `string` | no | Paging cursor for the next search page. |
| `sorts[]` | body | `array<string>` | no | Sort clauses to apply to the search results. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple comparison values for IN and NOT_IN filters. |
| `filterGroups[].filters[].highValue` | body | `string` | no | Upper bound value for BETWEEN filters. |
