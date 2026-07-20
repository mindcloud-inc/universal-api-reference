# Monta: Get Current Application

Retrieves the current application from Monta.

```
GET https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-current-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monta `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-current-application?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monta/latest/actions/get-current-application?${params}`, {
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
      "clientId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `scopes` | array<string> |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Monta API, this operation is `GET /auth/me` (base URL `https://public-api.monta.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-application.md) for the provider-specific parameters and requirements.

