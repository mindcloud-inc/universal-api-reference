# Kit: List Sequence Subscribers

Lists subscribers for a Kit sequence.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-sequence-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-sequence-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0&sequence_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sequence_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-sequence-subscribers?${params}`, {
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
| `sequence_id` | number | yes | Sequence ID from path parameter. |
| `status` | string | no | Filter by subscriber status. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `per_page` | number | no | Number of results per page (default 500, max 1000). |
| `after` | string | no | Fetch next page using end_cursor. |
| `before` | string | no | Fetch previous page using start_cursor. |
| `include_total_count` | boolean | no | Include total count in response. |
| `created_after` | date | no | Filter subscribers created after timestamp. |
| `created_before` | date | no | Filter subscribers created before timestamp. |
| `added_after` | date | no | Filter subscribers added to sequence after timestamp. |
| `added_before` | date | no | Filter subscribers added to sequence before timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kit API returns.

## Native endpoint

Through the native Kit API, this operation is `GET /sequences/:sequence_id/subscribers` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sequence-subscribers.md) for the provider-specific parameters and requirements.

