# Messaggio: Validate Credentials

Validates stored Messaggio credentials against the bulk API.

```
GET https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/validate-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Messaggio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messaggio/latest/actions/validate-credentials?${params}`, {
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
      "code": "string",
      "techMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Messaggio bulk response code. |
| `techMessage` | string | Provider technical message returned by the bounded validation request. |

## Native endpoint

Through the native Messaggio API, this operation is `GET https://bulk.sms-online.com/` (base URL `https://msg.messaggio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-credentials.md) for the provider-specific parameters and requirements.

