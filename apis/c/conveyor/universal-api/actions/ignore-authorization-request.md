# Conveyor: Ignore Authorization Request

Marks an authorization request as ignored in Conveyor.

```
PUT https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/ignore-authorization-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/ignore-authorization-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authorizationRequestId": "string",
  "reviewerEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/ignore-authorization-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authorizationRequestId": "string",
    "reviewerEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorizationRequestId` | string | yes | Authorization request identifier. |
| `reviewerEmail` | string | yes | Reviewer email for the status update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {
        "self": {}
      },
      "_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "dataroom_id": "string",
      "email": "ava@example.com",
      "id": "string",
      "message": "string",
      "requested_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `_links.self` | object |  |
| `_type` | string |  |
| `created_at` | date |  |
| `dataroom_id` | string |  |
| `email` | string |  |
| `id` | string |  |
| `message` | string |  |
| `requested_at` | date |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Conveyor API, this operation is `PATCH /v2/exchange/authorization_requests/:authorization_request_id` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ignore-authorization-request.md) for the provider-specific parameters and requirements.

