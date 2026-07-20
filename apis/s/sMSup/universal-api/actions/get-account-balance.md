# SMSup: Get Account Balance



```
GET https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-account-balance?${params}`, {
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
      "balance": "string",
      "currency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string | Current account balance. |
| `currency` | string | Currency code for the balance. |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/account/get-balance` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-balance.md) for the provider-specific parameters and requirements.

