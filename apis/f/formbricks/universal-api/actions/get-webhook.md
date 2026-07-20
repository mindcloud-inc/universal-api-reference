# Formbricks: Get Webhook

Retrieves a webhook from Formbricks.

```
GET https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | The ID of the webhook. |

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
| `data` | object | Webhook returned by the Formbricks management API. |
| `data.createdAt` | date | Timestamp when the webhook was created. |
| `data.environmentId` | string | Environment ID that owns the webhook. |
| `data.id` | string | Unique identifier of the webhook. |
| `data.name` | string | Name of the webhook. |
| `data.source` | string | Source of the webhook. |
| `data.surveyIds` | array<string> | Survey IDs associated with the webhook. |
| `data.triggers` | array<string> | Webhook trigger types. |
| `data.updatedAt` | date | Timestamp when the webhook was last updated. |
| `data.url` | string | Destination URL of the webhook. |

## Native endpoint

Through the native Formbricks API, this operation is `GET /management/webhooks/:id` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

