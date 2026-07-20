# FillFaster: Unsubscribe Webhook

Removes a webhook URL from a FillFaster form.

```
DELETE https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/unsubscribe-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FillFaster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/unsubscribe-webhook?connectionId=$CONNECTION_ID&formId=string&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string",
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/unsubscribe-webhook?${params}`, {
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
| `formId` | string | yes | FillFaster form identifier. |
| `url` | string | yes | Webhook destination URL to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message when the request fails. |
| `message` | string | Success message from FillFaster. |

## Native endpoint

Through the native FillFaster API, this operation is `POST /v1/form/:formId/webhook/unsubscribe` (base URL `https://api.fillfaster.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-webhook.md) for the provider-specific parameters and requirements.

