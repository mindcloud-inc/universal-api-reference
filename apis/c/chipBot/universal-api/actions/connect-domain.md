# ChipBot: Connect Domain



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/connect-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/connect-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/connect-domain?${params}`, {
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
      "data": {
        "accountId": "string",
        "apiKey": "string",
        "domainId": "string",
        "domainName": "Ava Chen",
        "expiresIn": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "token": "string",
        "type": "string"
      },
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Bootstrap token payload. |
| `data.accountId` | string | Resolved account identifier. |
| `data.apiKey` | string | Masked API key reference. |
| `data.domainId` | string | Resolved domain identifier. |
| `data.domainName` | string | Resolved domain name. |
| `data.expiresIn` | date | Token expiry timestamp. |
| `data.id` | string | Bootstrap token reference identifier. |
| `data.token` | string | Short-lived access token for domain API calls. |
| `data.type` | string | Bootstrap token scope type. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `POST /api/v1/connect` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-domain.md) for the provider-specific parameters and requirements.

