# Bulldog-WP: Get webhooks

Retrieves webhooks from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-webhooks?${params}`, {
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
      "device": {},
      "id": "string",
      "lastFailureAt": "2026-05-07T12:00:00.000Z",
      "lastRetryAt": "2026-05-07T12:00:00.000Z",
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "retries": 1,
      "status": 1,
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | object |  |
| `id` | string |  |
| `lastFailureAt` | date |  |
| `lastRetryAt` | date |  |
| `lastRunAt` | date |  |
| `name` | string |  |
| `retries` | number |  |
| `status` | number |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /webhooks` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-webhooks.md) for the provider-specific parameters and requirements.

