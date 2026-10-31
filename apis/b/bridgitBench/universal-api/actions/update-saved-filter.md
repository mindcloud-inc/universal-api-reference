# Bridgit Bench: Update Saved Filter



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-saved-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-saved-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "id": 1,
  "filtersSet[].type": "People",
  "filtersSet[].filterType": "string",
  "filtersSet[].filters[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-saved-filter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "id": 1,
    "filtersSet[].type": "People",
    "filtersSet[].filterType": "string",
    "filtersSet[].filters[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `id` | number | yes | Id of the filter to remove |
| `name` | string | no |  |
| `filtersSet[]` | array<object> | no |  |
| `filtersSet[].type` | list<string> | yes | One of: `People`, `Project`, `Roles`. |
| `filtersSet[].fieldDefId` | number | no |  |
| `filtersSet[].filterType` | string | yes |  |
| `filtersSet[].filters[]` | array<object> | yes |  |
| `filtersSet[].filters[].verb` | list<string> | no | One of: `Above`, `Below`, `Between`, `Equals`, `Excludes`, `Includes`. |
| `filtersSet[].filters[].valueIds[]` | array<number> | no |  |
| `filtersSet[].filters[].shortValues[]` | array<number> | no |  |
| `filtersSet[].filters[].intValues[]` | array<number> | no |  |
| `filtersSet[].filters[].longValues[]` | array<number> | no |  |
| `filtersSet[].filters[].decimalValues[]` | array<number> | no |  |
| `filtersSet[].filters[].dateValues[]` | array<date> | no |  |
| `filtersSet[].filters[].stringValue` | string | no |  |
| `filtersSet[].filters[].blankValue` | boolean | no |  |
| `filtersSet[].filters[].dynamicData` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PATCH /rp/api/v1/accounts/:accountId/my-filters/:id` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-saved-filter.md) for the provider-specific parameters and requirements.

