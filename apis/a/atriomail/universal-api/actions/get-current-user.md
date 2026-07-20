# Atriomail: Get Current User



```
GET https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Atriomail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/atriomail/latest/actions/get-current-user?${params}`, {
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
      "fraudStatus": "string",
      "id": 1,
      "lastLoginAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "paymentStatus": "string",
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Timestamp when the user was created. |
| `email` | string | Email address of the current AtrioMail user. |
| `fraudStatus` | string | Current fraud-review status for the AtrioMail account. |
| `id` | number | AtrioMail user ID. |
| `lastLoginAt` | date | Timestamp of the user's last login. |
| `name` | string | Display name of the current AtrioMail user. |
| `paymentStatus` | string | Current payment status for the AtrioMail account. |
| `role` | string | Role assigned to the current AtrioMail user. |
| `updatedAt` | date | Timestamp when the user was last updated. |

## Native endpoint

Through the native Atriomail API, this operation is `GET /user` (base URL `https://system.atriomail.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

