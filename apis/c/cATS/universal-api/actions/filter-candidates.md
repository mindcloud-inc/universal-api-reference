# CATS: Filter Candidates

Finds candidates in CATS by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/filter-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/filter-candidates?connectionId=$CONNECTION_ID&field=first_name&filter=contains&value=MindCloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field": "first_name",
  "filter": "contains",
  "value": "MindCloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/filter-candidates?${params}`, {
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
| `field` | string | yes | The field to filter on. Example: `first_name`. |
| `filter` | string | yes | The filter operator to use. Example: `contains`. |
| `value` | string | yes | The value to filter by. Example: `MindCloud`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `POST /candidates/search` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-candidates.md) for the provider-specific parameters and requirements.

