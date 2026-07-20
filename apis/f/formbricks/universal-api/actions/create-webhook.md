# Formbricks: Create Webhook

Creates a new webhook in Formbricks.

```
POST https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com",
  "source": "user",
  "environmentId": "string",
  "triggers[]": [
    "string"
  ],
  "surveyIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com",
    "source": "user",
    "environmentId": "string",
    "triggers[]": ["string"],
    "surveyIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the webhook. |
| `url` | string | yes | The destination URL of the webhook. |
| `source` | string | yes | The source of the webhook. Default: `user`. |
| `environmentId` | string | yes | The environment ID that owns the webhook. |
| `triggers[]` | array<string> | yes | Webhook trigger types. |
| `surveyIds[]` | array<string> | yes | Survey IDs associated with the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "environmentId": "string",
        "id": "string",
        "name": "Ava Chen",
        "source": "string",
        "surveyIds": [
          "string"
        ],
        "triggers": [
          "string"
        ],
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Webhook created by the Formbricks management API. |
| `data.createdAt` | date | Timestamp when the webhook was created. |
| `data.environmentId` | string | Environment ID that owns the created webhook. |
| `data.id` | string | Unique identifier of the created webhook. |
| `data.name` | string | Name of the created webhook. |
| `data.source` | string | Source of the created webhook. |
| `data.surveyIds` | array<string> | Survey IDs associated with the created webhook. |
| `data.triggers` | array<string> | Webhook trigger types. |
| `data.updatedAt` | date | Timestamp when the webhook was last updated. |
| `data.url` | string | Destination URL of the created webhook. |

## Native endpoint

Through the native Formbricks API, this operation is `POST /management/webhooks` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

