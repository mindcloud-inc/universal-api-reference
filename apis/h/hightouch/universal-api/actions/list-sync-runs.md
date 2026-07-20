# Hightouch: List Sync Runs

Retrieves sync runs from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-sync-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-sync-runs?connectionId=$CONNECTION_ID&limit=25&offset=0&syncId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "syncId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/list-sync-runs?${params}`, {
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
| `syncId` | number | yes | The sync ID. |
| `runId` | number | no | Query for a specific sync run ID. |
| `after` | date | no | Select sync runs started after this ISO timestamp. |
| `before` | date | no | Select sync runs started before this ISO timestamp. |
| `within` | number | no | Select sync runs started within the last given number of minutes. |

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
| `data` | array<object> | Sync run records returned by Hightouch. |
| `hasMore` | boolean | Whether more results are available. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /syncs/{syncId}/runs` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sync-runs.md) for the provider-specific parameters and requirements.

