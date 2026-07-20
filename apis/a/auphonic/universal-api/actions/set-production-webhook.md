# Auphonic: Set Production Webhook

Sets a production webhook in Auphonic.

```
PUT https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/set-production-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/set-production-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string",
  "webhook": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/set-production-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string",
    "webhook": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID of the production. |
| `webhook` | string | yes | Webhook callback URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhook` | string |  |

## Native endpoint

Through the native Auphonic API, this operation is `POST /production/:uuid/webhook.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-production-webhook.md) for the provider-specific parameters and requirements.

