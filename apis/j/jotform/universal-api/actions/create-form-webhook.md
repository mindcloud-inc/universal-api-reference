# Jotform: Create Form Webhook

Creates a webhook for a Jotform form.

```
POST https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "webhookURL": "https://example.com/jotform/webhook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jotform/latest/actions/create-form-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "webhookURL": "https://example.com/jotform/webhook"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Form ID |
| `webhookURL` | string | yes | Destination URL to receive webhook events. Example: `https://example.com/jotform/webhook`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "0": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `0` | string | Created webhook URL. |

## Native endpoint

Through the native Jotform API, this operation is `POST /form/:formId/webhooks` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form-webhook.md) for the provider-specific parameters and requirements.

