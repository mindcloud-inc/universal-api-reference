# Slottable: Create Webhook

Creates a new webhook in Slottable.

```
POST https://connect.mindcloud.co/v1/universal/slottable/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slottable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slottable/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data.url": "https://example.com/webhooks/slottable",
  "data.model": "Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slottable/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "data.url": "https://example.com/webhooks/slottable",
    "data.model": "Contact"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Company id returned by Slottable token details. |
| `data.url` | string | yes | Target URL that Slottable should call. Example: `https://example.com/webhooks/slottable`. |
| `data.model` | string | yes | Slottable model name to subscribe (for example Contact). Example: `Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "company_id": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "events": [
          "string"
        ],
        "filter_key": "string",
        "id": 1,
        "method": "string",
        "model": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.company_id` | number | Company id associated with the webhook. |
| `attributes.created_at` | date | Webhook creation timestamp. |
| `attributes.events` | array<string> | Subscribed webhook events. |
| `attributes.filter_key` | string | Optional filter key for webhook routing. |
| `attributes.id` | number | Webhook numeric id. |
| `attributes.method` | string | Webhook HTTP method. |
| `attributes.model` | string | Subscribed Slottable model. |
| `attributes.updated_at` | date | Webhook last update timestamp. |
| `attributes.url` | string | Webhook callback URL. |
| `id` | string | Webhook resource id. |
| `type` | string | JSON:API resource type. |

## Native endpoint

Through the native Slottable API, this operation is `POST /companies/:companyId/webhooks` (base URL `https://slottable.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

