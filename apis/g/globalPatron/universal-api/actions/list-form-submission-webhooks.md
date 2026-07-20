# Global Patron: List Form Submission Webhooks

Lists form submission webhooks in Global Patron.

```
GET https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-submission-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Global Patron `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-submission-webhooks?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-form-submission-webhooks?${params}`, {
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
| `formId` | string | yes | ID of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formId": "string",
      "httpHeaderKey": "string",
      "httpHeaderValue": "string",
      "id": "string",
      "webhookDestinationUrl": "https://example.com",
      "webhookName": "Ava Chen",
      "webhookSharedSecret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | string | Form identifier. |
| `httpHeaderKey` | string | Optional custom header key. |
| `httpHeaderValue` | string | Optional custom header value. |
| `id` | string | Webhook identifier. |
| `webhookDestinationUrl` | string | Webhook destination URL. |
| `webhookName` | string | Webhook display name. |
| `webhookSharedSecret` | string | Optional webhook shared secret. |

## Native endpoint

Through the native Global Patron API, this operation is `GET /api/restricted/form/{formId}/submissionwebhook` (base URL `https://api.globalpatron.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submission-webhooks.md) for the provider-specific parameters and requirements.

