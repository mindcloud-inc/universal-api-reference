# Postman: Get Mock Server

Retrieves details for a mock server from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-mock-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-mock-server?connectionId=$CONNECTION_ID&mockId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mockId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-mock-server?${params}`, {
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
| `mockId` | string | yes | The mock server's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mock": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "isPublic": true,
        "mockUrl": "https://example.com",
        "name": "Ava Chen",
        "uid": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mock.createdAt` | date |  |
| `mock.id` | string |  |
| `mock.isPublic` | boolean |  |
| `mock.mockUrl` | string |  |
| `mock.name` | string |  |
| `mock.uid` | string |  |
| `mock.updatedAt` | date |  |

## Native endpoint

Through the native Postman API, this operation is `GET /mocks/:mockId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mock-server.md) for the provider-specific parameters and requirements.

