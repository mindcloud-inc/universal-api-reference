# Zeplin: Get Styleguide Webhook

Retrieves a styleguide webhook from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-webhook?connectionId=$CONNECTION_ID&styleguideId=string&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "styleguideId": "string",
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/get-styleguide-webhook?${params}`, {
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
| `styleguideId` | string | yes | Styleguide id |
| `webhookId` | string | yes | Webhook id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "created_by": {},
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated": 1,
      "updated_by": {},
      "url": "https://example.com",
      "url_health": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `created_by` | object |  |
| `events` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated` | number |  |
| `updated_by` | object |  |
| `url` | string |  |
| `url_health` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/webhooks/{webhook_id}` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-styleguide-webhook.md) for the provider-specific parameters and requirements.

