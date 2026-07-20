# KleverKey: Add Webhook



```
POST https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": 1,
  "name": "Ava Chen",
  "requestMethod": "string",
  "requestUrl": "https://example.com",
  "eventTypes[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": 1,
    "name": "Ava Chen",
    "requestMethod": "string",
    "requestUrl": "https://example.com",
    "eventTypes[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | number | yes |  |
| `name` | string | yes |  |
| `requestMethod` | string | yes |  |
| `requestUrl` | string | yes |  |
| `eventTypes[]` | array<number> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "eventTypes": [
        1
      ],
      "id": 1,
      "isDisabled": true,
      "name": "Ava Chen",
      "organizationId": 1,
      "requestMethod": "string",
      "requestUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date |  |
| `eventTypes` | array<number> |  |
| `id` | number |  |
| `isDisabled` | boolean |  |
| `name` | string |  |
| `organizationId` | number |  |
| `requestMethod` | string |  |
| `requestUrl` | string |  |

## Native endpoint

Through the native KleverKey API, this operation is `POST /api/v1/organizations/:organizationId/webhooks` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook.md) for the provider-specific parameters and requirements.

