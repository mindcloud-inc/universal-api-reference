# SMSGlobal: List Pending Verified Numbers

Retrieves pending verified numbers from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-pending-verified-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-pending-verified-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-pending-verified-numbers?${params}`, {
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
      "numbers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numbers` | array<string> | Pending verified numbers for the authenticated account. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/user/verified-numbers/pending` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-verified-numbers.md) for the provider-specific parameters and requirements.

