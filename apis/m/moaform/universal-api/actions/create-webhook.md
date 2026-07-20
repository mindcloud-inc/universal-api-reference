# Moaform: Create Webhook

Creates a webhook for a form in Moaform.

```
POST https://connect.mindcloud.co/v1/universal/moaform/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moaform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moaform/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "endpoint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moaform/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "endpoint": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Unique ID of the form. |
| `endpoint` | string | yes | Webhook receiver URL. |
| `enabled` | boolean | no | Webhook activation status. |
| `secret` | string | no | Secret code for signing webhook payloads. |
| `verifySsl` | boolean | no | Whether to verify the endpoint SSL certificate. |
| `retentionDays` | number | no | Resend restriction days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "endpoint": "string",
      "id": "string",
      "retentionDays": 1,
      "secret": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verifySsl": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `endpoint` | string |  |
| `id` | string |  |
| `retentionDays` | number |  |
| `secret` | string |  |
| `updatedAt` | date |  |
| `verifySsl` | boolean |  |

## Native endpoint

Through the native Moaform API, this operation is `POST /forms/:formId/webhooks` (base URL `https://api.moaform.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

