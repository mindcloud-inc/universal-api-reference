# Kit: List Subscribers

Lists subscribers in your Kit account.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-subscribers?${params}`, {
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
| `after` | string | no | Pagination cursor to fetch subscribers after this position. |
| `before` | string | no | Pagination cursor to fetch subscribers before this position. |
| `page` | number | no | Page number for paginated subscriber results. |
| `perPage` | number | no | Number of subscribers to return per page. |
| `createdAfter` | date | no | Only include subscribers created after this timestamp. |
| `createdBefore` | date | no | Only include subscribers created before this timestamp. |
| `updatedAfter` | date | no | Only include subscribers updated after this timestamp. |
| `updatedBefore` | date | no | Only include subscribers updated before this timestamp. |
| `emailAddress` | string | no | Filter by an exact subscriber email address. |
| `status` | list<string> | no | Filter subscribers by lifecycle status. One of: `active`, `bounced`, `cancelled`, `complained`, `inactive`. |
| `sortField` | list<string> | no | Subscriber field used for sorting results. One of: `created_at`, `email_address`, `first_name`, `last_name`, `state`. |
| `sortOrder` | list<string> | no | Sort direction for subscriber results. One of: `asc`, `desc`. |
| `includeTotalCount` | boolean | no | Whether to include total count metadata in the response. |

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
      "subscribers": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "email_address": "ava@example.com",
          "fields": {},
          "first_name": "Ava",
          "id": 1,
          "state": "string"
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
| `pagination` | object |  |
| `pagination.end_cursor` | string |  |
| `pagination.has_next_page` | boolean |  |
| `pagination.has_previous_page` | boolean |  |
| `pagination.per_page` | number |  |
| `pagination.start_cursor` | string |  |
| `subscribers` | array<object> |  |
| `subscribers[].created_at` | date |  |
| `subscribers[].email_address` | string |  |
| `subscribers[].fields` | object |  |
| `subscribers[].first_name` | string |  |
| `subscribers[].id` | number |  |
| `subscribers[].state` | string |  |

## Native endpoint

Through the native Kit API, this operation is `GET /subscribers` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

