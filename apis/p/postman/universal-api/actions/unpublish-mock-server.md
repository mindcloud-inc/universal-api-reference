# Postman: Unpublish Mock Server

Sets a mock server to private in Postman.

```
PUT https://connect.mindcloud.co/v1/universal/postman/latest/actions/unpublish-mock-server
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postman/latest/actions/unpublish-mock-server" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mockId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postman/latest/actions/unpublish-mock-server', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mockId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mock.id` | string |  |

## Native endpoint

Through the native Postman API, this operation is `DELETE /mocks/:mockId/unpublish` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unpublish-mock-server.md) for the provider-specific parameters and requirements.

