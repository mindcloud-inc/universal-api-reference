# Relevance AI: Get Workforce



```
GET https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Relevance AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce?connectionId=$CONNECTION_ID&workforceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workforceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/get-workforce?${params}`, {
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
| `workforceId` | string | yes | The Relevance AI workforce id to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "project": "string",
      "workforce_graph": {
        "edges": [
          {}
        ],
        "nodes": [
          {}
        ]
      },
      "workforce_metadata": {
        "active_version_id": "string",
        "last_run_date": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "thumbnail_url": "https://example.com",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The workforce ID. |
| `project` | string | The Relevance AI project ID. |
| `workforce_graph.edges` | array<object> | The workforce graph edges. |
| `workforce_graph.nodes` | array<object> | The workforce graph nodes. |
| `workforce_metadata.active_version_id` | string | The active version ID. |
| `workforce_metadata.last_run_date` | date | The last run timestamp for the workforce. |
| `workforce_metadata.name` | string | The workforce display name. |
| `workforce_metadata.thumbnail_url` | string | The workforce thumbnail or emoji. |
| `workforce_metadata.type` | string | The workforce type. |

## Native endpoint

Through the native Relevance AI API, this operation is `GET /workforce/items/:workforceId` (base URL `https://api-{{credentials.region}}.stack.tryrelevance.com/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workforce.md) for the provider-specific parameters and requirements.

