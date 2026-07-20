# Postman: Create Mock Server

Creates a new mock server in Postman.

```
POST https://connect.mindcloud.co/v1/universal/postman/latest/actions/create-mock-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postman/latest/actions/create-mock-server" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mock.name": "Ava Chen",
  "mock.collection": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postman/latest/actions/create-mock-server', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mock.name": "Ava Chen",
    "mock.collection": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspace` | string | no |  |
| `mock.name` | string | yes |  |
| `mock.collection` | string | yes |  |
| `mock.environment` | string | no |  |
| `mock.private` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mock": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
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
| `mock.mockUrl` | string |  |
| `mock.name` | string |  |
| `mock.uid` | string |  |
| `mock.updatedAt` | date |  |

## Native endpoint

Through the native Postman API, this operation is `POST /mocks` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-mock-server.md) for the provider-specific parameters and requirements.

