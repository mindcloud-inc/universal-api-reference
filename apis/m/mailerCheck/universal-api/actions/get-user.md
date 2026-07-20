# MailerCheck: Get User

Retrieves the current user from MailerCheck.

```
GET https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-user?${params}`, {
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
      "emailVerifiedAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "subscribedNewsletter": 1,
      "termsAcceptedAt": "string",
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
| `emailVerifiedAt` | date |  |
| `id` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `subscribedNewsletter` | number |  |
| `termsAcceptedAt` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native MailerCheck API, this operation is `GET /user` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

