# Typeform: Retrieve Single Webhook



```
GET https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-single-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-single-webhook?connectionId=$CONNECTION_ID&formId=string&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeform/latest/actions/retrieve-single-webhook?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | Typeform form identifier. |
| `tag` | string | yes | Webhook tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "eventTypes": {
        "formResponse": true
      },
      "formId": "string",
      "id": "string",
      "secret": "string",
      "tag": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "verifySsl": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `enabled` | boolean | Whether webhook is enabled. |
| `eventTypes` | object | Webhook event type configuration. |
| `eventTypes.formResponse` | boolean | Whether form_response events are enabled. |
| `formId` | string | Form ID. |
| `id` | string | Webhook ID. |
| `secret` | string | Webhook secret. |
| `tag` | string | Webhook tag. |
| `updatedAt` | date | Last update timestamp. |
| `url` | string | Webhook destination URL. |
| `verifySsl` | boolean | Whether SSL verification is enabled. |

## Native endpoint

Through the native Typeform API, this operation is `GET /forms/:formId/webhooks/:tag` (base URL `https://api.typeform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-single-webhook.md) for the provider-specific parameters and requirements.

