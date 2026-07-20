# Hightouch: List IDR Runs

Retrieves IDR runs from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-idr-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-idr-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&graphId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "graphId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-idr-runs?${params}`, {
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
| `graphId` | string | yes | The IDR graph ID. |
| `runId` | string | no | Filter IDR runs by run ID. |
| `after` | date | no | Select IDR runs after this ISO timestamp. |
| `before` | date | no | Select IDR runs before this ISO timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | IDR run records returned by Hightouch. |
| `hasMore` | boolean | Whether more results are available. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /idr/{graphId}/runs` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-idr-runs.md) for the provider-specific parameters and requirements.

