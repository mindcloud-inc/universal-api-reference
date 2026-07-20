# FEMA: List OpenFEMA Data Sets

Retrieves OpenFEMA data sets from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-openfema-data-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-openfema-data-sets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-openfema-data-sets?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "api": true,
      "contactPoint": "Ava Chen",
      "dataDictionary": "https://example.com",
      "description": "string",
      "distribution": [
        {}
      ],
      "id": "string",
      "identifier": "string",
      "keyword": [
        "string"
      ],
      "lastDataSetRefresh": "2026-05-07T12:00:00.000Z",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "mbox": "ava@example.com",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "publisher": "Ava Chen",
      "recordCount": 1,
      "theme": "string",
      "title": "string",
      "version": 1,
      "webService": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `api` | boolean |  |
| `contactPoint` | string |  |
| `dataDictionary` | string |  |
| `description` | string |  |
| `distribution` | array<object> |  |
| `id` | string |  |
| `identifier` | string |  |
| `keyword` | array<string> |  |
| `lastDataSetRefresh` | date |  |
| `lastRefresh` | date |  |
| `mbox` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `publisher` | string |  |
| `recordCount` | number |  |
| `theme` | string |  |
| `title` | string |  |
| `version` | number |  |
| `webService` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/DataSets` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-openfema-data-sets.md) for the provider-specific parameters and requirements.

