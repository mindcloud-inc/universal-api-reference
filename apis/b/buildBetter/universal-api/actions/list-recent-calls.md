# BuildBetter: List Recent Calls



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-recent-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-recent-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-recent-calls?${params}`, {
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
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "short_summary": "string",
      "source": "string",
      "transcript_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `display_ts` | date | Display timestamp for the call. |
| `id` | string | BuildBetter call identifier. |
| `name` | string | Call title. |
| `short_summary` | string | Brief AI summary. |
| `source` | string | Source system for the call. |
| `transcript_status` | string | Transcript processing status. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-calls.md) for the provider-specific parameters and requirements.

