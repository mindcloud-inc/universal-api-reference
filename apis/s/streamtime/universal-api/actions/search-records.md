# Streamtime: Search Records



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/search-records?connectionId=$CONNECTION_ID&searchView=12&filterGroupCollection=%5Bobject%20Object%5D&filterGroupCollection.conditionMatchTypeId=1&filterGroupCollection.filterGroups%5B%5D=" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "searchView": "12",
  "filterGroupCollection": "[object Object]",
  "filterGroupCollection.conditionMatchTypeId": "1",
  "filterGroupCollection.filterGroups[]": ""
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/search-records?${params}`, {
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
| `searchView` | number | yes | Search view enum that selects which record domain to search. Example: `12`. |
| `wildcardSearch` | string | no | Free-text search string applied within the selected search view. Example: `Codex Stage3 Company 20260312T1812`. |
| `offset` | number | no | Result offset for the search request. Default: `0`. Example: `0`. |
| `maxResults` | number | no | Maximum number of results to return. Example: `5`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeStatistics` | boolean | no | Whether to include the optional statistics object in the response. |
| `sortField` | number | no | Search column enum to sort by. Example: `1`. |
| `sortAscending` | boolean | no | Whether sort order should be ascending. |
| `filterGroupCollection` | object | yes | Advanced recursive filter DSL object documented by Streamtime for structured searches. |
| `filterGroupCollection.conditionMatchTypeId` | number | yes | AND/OR enum for the root filter group collection. Example: `1`. |
| `filterGroupCollection.filterGroups[]` | array<object> | yes | Array of filter groups. Streamtime runtime requires this key to be present even for wildcard-only searches. Default: `[]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Streamtime API returns.

## Native endpoint

Through the native Streamtime API, this operation is `POST /search` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

