# 3E Protect: Search Catalog Items



```
GET https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/search-catalog-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/search-catalog-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/search-catalog-items?${params}`, {
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
| `locationName` | object | no | Filter by an existing 3E location name. Find names with List Locations. |
| `locationName.value` | string | no | Location name returned by List Locations. |
| `locationName.compareOption` | list<string> | no | Choose Equals for an exact location name or another documented comparison. One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productName` | object | no |  |
| `productName.value` | string | no |  |
| `productName.compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `manufacturerName` | object | no |  |
| `manufacturerName.value` | string | no |  |
| `manufacturerName.compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `manufacturerPartNumber` | object | no |  |
| `manufacturerPartNumber.value` | string | no |  |
| `manufacturerPartNumber.compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `casNumber` | object | no | CAS means Chemical Abstracts Service; its registry number identifies a chemical substance. |
| `casNumber.value` | string | no |  |
| `casNumber.compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `sdsCountry` | object | no |  |
| `sdsCountry.value` | string | no |  |
| `sdsCountry.compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `uniqueIdentifiers[]` | array<object> | no | Filter using customer product identifier source and value pairs. Sources are available from List Product Identifier Sources. |
| `uniqueIdentifiers[].source` | string | no |  |
| `uniqueIdentifiers[].value` | string | no |  |
| `uniqueIdentifiers[].compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `customValues[]` | array<object> | no | Filter customer-defined fields by name, value and comparison. Field names are available from List Custom Value Names. |
| `customValues[].name` | string | no |  |
| `customValues[].value` | string | no |  |
| `customValues[].compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |
| `lastAlteredDate` | object | no |  |
| `lastAlteredDate.valueMin` | date | no |  |
| `lastAlteredDate.valueMax` | date | no |  |
| `lastAlteredDate.compareOption` | list<string> | no | One of: `BeginsWith`, `Between`, `Contains`, `Equals`, `GreaterThan`, `LessThan`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `POST /document-search` (base URL `{{credentials.documentSearchApiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-catalog-items.md) for the provider-specific parameters and requirements.

