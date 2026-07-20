# KnowledgeOwl: Get Webhook Subscription



```
GET https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/get-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/get-webhook-subscription?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/get-webhook-subscription?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "date_created": "2026-05-07T12:00:00.000Z",
        "date_deleted": "2026-05-07T12:00:00.000Z",
        "date_modified": "2026-05-07T12:00:00.000Z",
        "endpoint": "string",
        "event": [
          [
            "string"
          ]
        ],
        "id": "string",
        "output": "string",
        "project_ids": [
          [
            "string"
          ]
        ],
        "restrict_to_category": "string",
        "status": "string",
        "token": "string",
        "type": "string"
      },
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.date_created` | date |  |
| `data.date_deleted` | date |  |
| `data.date_modified` | date |  |
| `data.endpoint` | string |  |
| `data.event[]` | array<string> |  |
| `data.id` | string |  |
| `data.output` | string |  |
| `data.project_ids[]` | array<string> |  |
| `data.restrict_to_category` | string |  |
| `data.status` | string |  |
| `data.token` | string |  |
| `data.type` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native KnowledgeOwl API, this operation is `GET /webhook/:id.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-subscription.md) for the provider-specific parameters and requirements.

