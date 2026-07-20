# Time Doctor: List User Tokens

Retrieves user tokens from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-user-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-user-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-user-tokens?${params}`, {
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
      "__v": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "ip": "string",
      "token": "string",
      "userAgent": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__v` | number |  |
| `createdAt` | date |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `ip` | string |  |
| `token` | string |  |
| `userAgent` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/users/tokens` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-tokens.md) for the provider-specific parameters and requirements.

