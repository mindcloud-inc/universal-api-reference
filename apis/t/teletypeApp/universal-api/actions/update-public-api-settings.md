# Teletype App: Update Public API Settings

Updates public API settings in Teletype App.

```
PUT https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/update-public-api-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teletype App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/update-public-api-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/update-public-api-settings', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiWebhook` | string | no | Webhook URL to store in the Teletype project public API settings. |
| `activeWebhooks[]` | array<string> | no | Webhook event names to enable for the Teletype project public API settings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean | Boolean result returned by Teletype after updating public API settings. |

## Native endpoint

Through the native Teletype App API, this operation is `POST /project/update-public-api` (base URL `https://api.teletype.app/public/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-public-api-settings.md) for the provider-specific parameters and requirements.

