# Overledger: Update Account Webhook Callback URL



```
PUT https://connect.mindcloud.co/v1/universal/overledger/latest/actions/update-account-webhook-callback-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Overledger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/overledger/latest/actions/update-account-webhook-callback-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string",
  "callbackUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/overledger/latest/actions/update-account-webhook-callback-url', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string",
    "callbackUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | Account webhook identifier to update. |
| `callbackUrl` | string | yes | New public callback URL for the account webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "location": {},
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string | Updated callback URL. |
| `callbackUrlStatus` | string | Callback URL status. |
| `location` | object | Blockchain location. |
| `webhookId` | string | Webhook identifier. |

## Native endpoint

Through the native Overledger API, this operation is `PATCH /api/webhooks/accounts/:webhookId` (base URL `https://api.overledger.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-webhook-callback-url.md) for the provider-specific parameters and requirements.

