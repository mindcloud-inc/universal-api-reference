# Instatus: Get User Profile



```
GET https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-user-profile?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Instatus API, this operation is `GET /v1/user` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-profile.md) for the provider-specific parameters and requirements.

