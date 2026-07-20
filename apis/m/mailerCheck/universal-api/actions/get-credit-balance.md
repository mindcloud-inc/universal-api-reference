# MailerCheck: Get Credit Balance

Retrieves account credit balance from MailerCheck.

```
GET https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-credit-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-credit-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerCheck/latest/actions/get-credit-balance?${params}`, {
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `total` | number |  |

## Native endpoint

Through the native MailerCheck API, this operation is `GET /credits` (base URL `https://app.mailercheck.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-credit-balance.md) for the provider-specific parameters and requirements.

