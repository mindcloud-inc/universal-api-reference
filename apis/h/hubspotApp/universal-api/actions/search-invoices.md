# HubSpot: Search Invoices

Finds invoices in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-invoices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-invoices?${params}`, {
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
| `query` | string | no | A free-text query for invoice search. Example: `INV-1001`. |
| `filterGroups` | object<object> | no | Provide the full HubSpot filterGroups array, for example [{"filters":[{"propertyName":"hs_object_id","operator":"EQ","value":"123"}]}]. |
| `filterGroups[].filters[]` | array<object> | no | The filters within a filter group. |
| `filterGroups[].filters[].propertyName` | string | no | The property name to filter on. Example: `hs_invoice_status`. |
| `filterGroups[].filters[].operator` | list | no | The operator to apply to the filter. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | string | no | The single comparison value for the filter. Example: `open`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple comparison values for operators that accept arrays. Example: `draft`. |
| `filterGroups[].filters[].highValue` | string | no | The upper bound value for range filters. Example: `2025-12-31`. |
| `after` | string | no | The pagination cursor to continue a prior search. Example: `opaque-cursor`. |
| `limit` | number | no | The number of results to return. Example: `10`. |
| `sorts[]` | array<string> | no | The list of sort definitions. Example: `-hs_lastmodifieddate`. |
| `properties[]` | array<string> | no | The properties to include in each invoice result. Example: `hs_invoice_status`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the invoice is archived. |
| `createdAt` | date | When the invoice was created. |
| `id` | string | The invoice record ID. |
| `properties` | object | The returned invoice properties. |
| `updatedAt` | date | When the invoice was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/invoices/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-invoices.md) for the provider-specific parameters and requirements.

