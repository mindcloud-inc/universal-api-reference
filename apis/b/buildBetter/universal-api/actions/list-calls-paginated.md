# BuildBetter: List Calls Paginated



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-calls-paginated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-calls-paginated?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-calls-paginated?${params}`, {
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
| `limit` | number | no | Maximum number of calls to return. Default: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Number of calls to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "recorded_at": "2026-05-07T12:00:00.000Z",
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
| `recorded_at` | date | Recording timestamp. |
| `short_summary` | string | Brief AI summary. |
| `source` | string | Source system for the call. |
| `transcript_status` | string | Transcript processing status. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calls-paginated.md) for the provider-specific parameters and requirements.

