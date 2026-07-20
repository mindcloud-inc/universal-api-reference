# Mailcheck: Rotate API Key



```
PUT https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/rotate-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/rotate-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/rotate-api-key', {
  method: 'PUT',
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
      "api_key": "string",
      "message": "string",
      "warning": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_key` | string | The newly issued MailCheck API key. |
| `message` | string | Rotation status message. |
| `warning` | string | Warning that the old key has been revoked. |

## Native endpoint

Through the native Mailcheck API, this operation is `POST /v1/account/rotate-key` (base URL `https://api.mailcheck.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rotate-api-key.md) for the provider-specific parameters and requirements.

