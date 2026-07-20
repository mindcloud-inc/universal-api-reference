# HubSpot: Search Tickets

Finds tickets in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-tickets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | The text query to match across searchable ticket properties. |
| `filterGroups` | object | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | array | no | Filters to apply within a filter group. |
| `filterGroups[].filters[].propertyName` | string | no | The property name to filter on. |
| `filterGroups[].filters[].operator` | list | no | The operator to apply to the filter. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | string | no | A single value for the filter. |
| `filterGroups[].filters[].highValue` | string | no | The upper bound value when using the BETWEEN operator. |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple values for IN or NOT_IN filters. |
| `sorts[]` | array | no | Sorting rules to apply to the search results. |
| `sorts[].propertyName` | string | no | The property name to sort by. |
| `sorts[].direction` | string | no | The sort direction. |
| `properties[]` | array<string> | no | Ticket property names to return in the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HubSpot API returns.

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/tickets/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

