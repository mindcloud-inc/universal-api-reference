# Conveyor: Get Authorization Request

Retrieves an authorization request from Conveyor.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/get-authorization-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/get-authorization-request?connectionId=$CONNECTION_ID&authorizationRequestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorizationRequestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/get-authorization-request?${params}`, {
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
| `authorizationRequestId` | string | yes | Authorization request identifier. |

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

Through the native Conveyor API, this operation is `GET /v2/exchange/authorization_requests/:authorization_request_id` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authorization-request.md) for the provider-specific parameters and requirements.

