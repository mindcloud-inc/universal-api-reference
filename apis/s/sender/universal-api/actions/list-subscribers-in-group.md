# Sender: List Subscribers in Group



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscribers-in-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscribers-in-group?connectionId=$CONNECTION_ID&limit=25&offset=0&id=grp_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "grp_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscribers-in-group?${params}`, {
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
| `id` | string | yes | Group ID. Example: `grp_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncedAt": "2026-05-07T12:00:00.000Z",
      "columns": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "ipAddress": "string",
      "lastname": "Chen",
      "location": "string",
      "phone": "string",
      "phoneCountry": "string",
      "source": "string",
      "status": {},
      "subscriberTags": [
        {}
      ],
      "unsubscribedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncedAt` | date |  |
| `columns` | array<object> |  |
| `created` | date |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `lastname` | string |  |
| `location` | string |  |
| `phone` | string |  |
| `phoneCountry` | string |  |
| `source` | string |  |
| `status` | object |  |
| `subscriberTags` | array<object> |  |
| `unsubscribedAt` | date |  |

## Native endpoint

Through the native Sender API, this operation is `GET /groups/:id/subscribers` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscribers-in-group.md) for the provider-specific parameters and requirements.

