# HubSpot: Search Contacts

Finds contacts in HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
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
| `emailContains` | string | no | Filter contacts whose email contains this value. For a domain, enter @mindcloud.co; the action sends HubSpot an email CONTAINS_TOKEN filter with the correct wildcard format. Example: `@mindcloud.co`. |
| `filterPropertyName` | list<string> | no | Choose any contact property to filter search results by. |
| `filterOperator` | list | no | Choose how to compare the selected contact property to the filter value. One of: `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`. Default: `EQ`. |
| `filterValue` | string | no | Enter the value to search for in the selected contact property. Example: `Alice`. |
| `properties` | list<string> | no | Select the contact properties to include in the response. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterGroups[].filters[]` | array<object> | no | Raw HubSpot filter group filters for advanced searches. Use these when you need multiple filters, AND/OR groups, IN/NOT_IN, or BETWEEN filtering. |
| `filterGroups[].filters[].propertyName` | list<string> | no | The HubSpot contact property name for an advanced raw filter. |
| `filterGroups[].filters[].operator` | list | no | The HubSpot search operator for an advanced raw filter. One of: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | string | no | The primary comparison value for an advanced raw filter. Required for operators such as EQ, CONTAINS_TOKEN, and the lower bound of BETWEEN. |
| `filterGroups[].filters[].values[]` | array<string> | no | Multiple values for IN or NOT_IN advanced filters. |
| `filterGroups[].filters[].highValue` | string | no | The upper bound for BETWEEN advanced filters. |

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

Through the native HubSpot API, this operation is `POST crm/v3/objects/contacts/search` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

