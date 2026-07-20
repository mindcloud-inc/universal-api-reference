# Hightouch: Get Sync Sequence Run

Retrieves a sync sequence run from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-sync-sequence-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-sync-sequence-run?connectionId=$CONNECTION_ID&syncSequenceRunId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "syncSequenceRunId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-sync-sequence-run?${params}`, {
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
| `syncSequenceRunId` | string | yes | The sync sequence run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "syncRuns": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Sync sequence run ID. |
| `status` | string | Sync sequence run status. |
| `syncRuns` | array<object> | Individual sync run statuses. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /sync-sequences/runs/{syncSequenceRunId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sync-sequence-run.md) for the provider-specific parameters and requirements.

