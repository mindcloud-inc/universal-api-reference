# Kit: List Tags for Subscriber

Lists tags for a Kit subscriber.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-tags-for-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-tags-for-subscriber?connectionId=$CONNECTION_ID&limit=25&offset=0&subscriberId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "subscriberId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-tags-for-subscriber?${params}`, {
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
| `subscriberId` | number | yes | Kit subscriber ID whose tags should be listed. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTotalCount` | boolean | no | Set to true to include total_count in the response. Kit notes this can make the request slower. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "end_cursor": "string",
        "has_next_page": true,
        "has_previous_page": true,
        "per_page": 1,
        "start_cursor": "string"
      },
      "tags": [
        {
          "id": 1,
          "name": "Ava Chen",
          "tagged_at": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Cursor pagination metadata. |
| `pagination.end_cursor` | string | Cursor for requesting the next page. |
| `pagination.has_next_page` | boolean | Whether a next page is available. |
| `pagination.has_previous_page` | boolean | Whether a previous page is available. |
| `pagination.per_page` | number | Returned page size. |
| `pagination.start_cursor` | string | Cursor for requesting the previous page. |
| `tags` | array<object> | Collection of tags assigned to the subscriber. |
| `tags[].id` | number | Tag ID. |
| `tags[].name` | string | Tag name. |
| `tags[].tagged_at` | date | Timestamp when the subscriber was tagged. |

## Native endpoint

Through the native Kit API, this operation is `GET /subscribers/:subscriber_id/tags` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags-for-subscriber.md) for the provider-specific parameters and requirements.

