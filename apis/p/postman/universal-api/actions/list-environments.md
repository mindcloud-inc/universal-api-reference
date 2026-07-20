# Postman: List Environments

Retrieves all accessible environments from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-environments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-environments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/list-environments?${params}`, {
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
      "environments": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "isPublic": true,
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
| `environments[].createdAt` | date |  |
| `environments[].id` | string |  |
| `environments[].isPublic` | boolean |  |
| `environments[].name` | string |  |
| `environments[].uid` | string |  |
| `environments[].updatedAt` | date |  |

## Native endpoint

Through the native Postman API, this operation is `GET /environments` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-environments.md) for the provider-specific parameters and requirements.

