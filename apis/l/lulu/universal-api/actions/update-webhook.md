# Lulu: Update Webhook

Updates an existing webhook in Lulu.

```
PUT https://connect.mindcloud.co/v1/universal/lulu/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "6b522ab9-31ec-4418-a904-95436160d4a8"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lulu/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "6b522ab9-31ec-4418-a904-95436160d4a8"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lulu webhook ID. Default: `6b522ab9-31ec-4418-a904-95436160d4a8`. |
| `topics[]` | array | no | Replacement Lulu webhook topic list. Default: `["PRINT_JOB_STATUS_CHANGED"]`. |
| `url` | string | no | Updated destination URL for the webhook. Default: `https://example.com/lulu/webhook-updated`. |
| `isActive` | boolean | no | Whether the webhook should remain active. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isActive": true,
      "topics": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isActive` | boolean |  |
| `topics` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Lulu API, this operation is `PATCH /webhooks/{id}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

