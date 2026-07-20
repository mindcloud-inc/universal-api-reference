# Sequenzy: List Subscribers

Retrieves a paginated list of subscribers from Sequenzy.

```
GET https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sequenzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/list-subscribers?${params}`, {
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
| `email` | string | no | Filter by partial email match. |
| `limit` | string | no | Items per page. Max 100. |
| `page` | string | no | Page number. |
| `status` | string | no | Filter by subscriber status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1,
        "totalPages": 1
      },
      "subscribers": {
        "createdAt": "string",
        "customAttributes": {},
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "status": "string",
        "tags": [
          "string"
        ],
        "updatedAt": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `subscribers` | array<object> |  |
| `subscribers.createdAt` | string |  |
| `subscribers.customAttributes` | object |  |
| `subscribers.email` | string |  |
| `subscribers.firstName` | string |  |
| `subscribers.id` | string |  |
| `subscribers.lastName` | string |  |
| `subscribers.status` | string |  |
| `subscribers.tags` | array<string> |  |
| `subscribers.updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sequenzy API, this operation is `GET /subscribers` (base URL `https://api.sequenzy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

