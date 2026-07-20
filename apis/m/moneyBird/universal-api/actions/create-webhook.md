# MoneyBird: Create Webhook

Creates a new webhook in MoneyBird.

```
POST https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "administrationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "administrationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `administrationId` | string | yes | Moneybird administration ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrationId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deactivatedAt": "2026-05-07T12:00:00.000Z",
      "enabledEvents": [
        "string"
      ],
      "id": "string",
      "lastHttpBody": "string",
      "lastHttpStatus": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrationId` | string |  |
| `createdAt` | date |  |
| `deactivatedAt` | date |  |
| `enabledEvents` | array<string> |  |
| `id` | string |  |
| `lastHttpBody` | string |  |
| `lastHttpStatus` | number |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native MoneyBird API, this operation is `POST /:administrationId/webhooks.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

