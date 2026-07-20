# Pitchbox: List Email Accounts



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-email-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-email-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/list-email-accounts?${params}`, {
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
      "createdByUser": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "id": 1
      },
      "dailyLimit": 1,
      "fromName": "Ava Chen",
      "id": 1,
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "status": "string",
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
| `createdByUser.displayName` | string |  |
| `createdByUser.email` | string |  |
| `createdByUser.id` | number |  |
| `dailyLimit` | number |  |
| `fromName` | string |  |
| `id` | number |  |
| `name` | string |  |
| `nickname` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/email_accounts` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-accounts.md) for the provider-specific parameters and requirements.

