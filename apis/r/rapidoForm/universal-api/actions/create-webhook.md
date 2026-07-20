# RapidoForm: Create Webhook

Creates a webhook for RapidoForm form submissions.

```
POST https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidoForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": "string",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rapidoForm/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": "string",
    "webhookUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | string | yes |  |
| `webhookUrl` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "isWebhookOn": true,
      "surveyId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string",
      "V": 1,
      "verifySSL": true,
      "webhookSecret": "string",
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `Id` | string |  |
| `isWebhookOn` | boolean |  |
| `surveyId` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |
| `V` | number |  |
| `verifySSL` | boolean |  |
| `webhookSecret` | string |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native RapidoForm API, this operation is `POST /api/webhook/save` (base URL `https://www.rapidoform.com/be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

