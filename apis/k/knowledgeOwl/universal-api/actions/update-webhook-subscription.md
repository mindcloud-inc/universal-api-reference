# KnowledgeOwl: Update Webhook Subscription



```
PUT https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "endpoint": "string",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-webhook-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "endpoint": "string",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `endpoint` | string | yes |  |
| `event` | list<string> | yes | Accepts multiple values as an array. |

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

Through the native KnowledgeOwl API, this operation is `PUT /webhook/:id.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-subscription.md) for the provider-specific parameters and requirements.

