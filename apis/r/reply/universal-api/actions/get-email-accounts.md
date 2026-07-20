# Reply: Get Email Accounts



```
GET https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-email-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-email-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reply/latest/actions/get-email-accounts?${params}`, {
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
      "emailAddress": "ava@example.com",
      "id": 1,
      "senderName": "Ava Chen",
      "signature": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string | Connected mailbox address. |
| `id` | number | Reply email account identifier. |
| `senderName` | string | Sender display name. |
| `signature` | string | Configured signature text. |

## Native endpoint

Through the native Reply API, this operation is `GET /v1/emailAccounts` (base URL `https://api.reply.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-accounts.md) for the provider-specific parameters and requirements.

