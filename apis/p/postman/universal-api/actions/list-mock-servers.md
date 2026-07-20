# Postman: List Mock Servers

Retrieves all mock servers from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-mock-servers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-mock-servers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-mock-servers?${params}`, {
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
      "mocks": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "isPublic": true,
          "mockUrl": "https://example.com",
          "name": "Ava Chen",
          "uid": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `mocks[].createdAt` | date |  |
| `mocks[].id` | string |  |
| `mocks[].isPublic` | boolean |  |
| `mocks[].mockUrl` | string |  |
| `mocks[].name` | string |  |
| `mocks[].uid` | string |  |
| `mocks[].updatedAt` | date |  |

## Native endpoint

Through the native Postman API, this operation is `GET /mocks` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mock-servers.md) for the provider-specific parameters and requirements.

