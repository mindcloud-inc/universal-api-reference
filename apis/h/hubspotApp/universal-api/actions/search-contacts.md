# HubSpot: Search Contacts

Finds contacts in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-contacts?${params}`, {
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
| `query` | string | no | The text to search across default searchable contact properties. |
| `filterGroups[].filters[]` | array<object> | no | Add a Property, Operator, and Value to filter your search results. Add additional filters in the same group for AND logic. |
| `filterGroups[].filters[].propertyName` | list<string> | no | The contact property to filter on. |
| `filterGroups[].filters[].operator` | list | no | The comparison operator used by the filter. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | string | no | The primary comparison value used by the filter. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple comparison values for list-style operators. |
| `filterGroups[].filters[].highValue` | string | no | The upper bound used by range filters. |
| `after` | string | no | The paging cursor for the next set of search results. |
| `limit` | number | no | The maximum number of contacts to return. |
| `sorts[]` | array<string> | no | Fields used to sort the returned contacts. |
| `properties[]` | array<string> | no | Contact properties to include in the response. |

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
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the contact is archived. |
| `createdAt` | date | When the contact was created. |
| `id` | string | The contact record ID. |
| `properties` | object | The returned contact properties. |
| `updatedAt` | date | When the contact was last updated. |
| `url` | string | The HubSpot record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/contacts/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

