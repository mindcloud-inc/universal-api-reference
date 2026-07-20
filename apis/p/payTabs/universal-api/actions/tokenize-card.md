# PayTabs: Tokenize Card



```
POST https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/tokenize-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/tokenize-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/tokenize-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cardScheme": "string",
      "code": 1,
      "currency": "string",
      "device": {},
      "message": "string",
      "payment": {},
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardScheme` | string |  |
| `code` | number |  |
| `currency` | string |  |
| `device` | object |  |
| `message` | string |  |
| `payment` | object |  |
| `token` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/tokenise` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tokenize-card.md) for the provider-specific parameters and requirements.

