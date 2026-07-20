# Conveyor: List Authorization Requests

Retrieves authorization requests from Conveyor with optional filters.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-authorization-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-authorization-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-authorization-requests?${params}`, {
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
| `email` | string | no | Email address filter. |
| `status` | string | no | Authorization request status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorization_requests": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": "string",
          "status": "string"
        }
      ],
      "page": 1,
      "per_page": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorization_requests` | array<object> |  |
| `authorization_requests[].created_at` | date |  |
| `authorization_requests[].email` | string |  |
| `authorization_requests[].id` | string |  |
| `authorization_requests[].status` | string |  |
| `page` | number |  |
| `per_page` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/exchange/authorization_requests` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-authorization-requests.md) for the provider-specific parameters and requirements.

