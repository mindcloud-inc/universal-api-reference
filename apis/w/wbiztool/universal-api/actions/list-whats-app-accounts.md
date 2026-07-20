# Wbiztool: List WhatsApp Accounts

Retrieves WhatsApp client accounts from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-whats-app-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-whats-app-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-whats-app-accounts?${params}`, {
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
      "status": "string",
      "whatsappClientId": 1,
      "whatsappNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `whatsappClientId` | number |  |
| `whatsappNumber` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /whatsapp/accounts/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whats-app-accounts.md) for the provider-specific parameters and requirements.

