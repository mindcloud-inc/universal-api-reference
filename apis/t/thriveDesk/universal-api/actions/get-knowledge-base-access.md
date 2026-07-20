# ThriveDesk: Get Knowledge Base Access



```
GET https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-knowledge-base-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-knowledge-base-access?connectionId=$CONNECTION_ID&knowledgebaseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "knowledgebaseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/get-knowledge-base-access?${params}`, {
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
| `knowledgebaseId` | string | yes | The knowledge base ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw response payload. |
| `id` | string | Knowledge Base Access identifier when returned. |
| `message` | string | Provider response message when returned. |
| `name` | string | Knowledge Base Access name when returned. |
| `status` | string | Knowledge Base Access status when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `GET /v1/knowledgebases/{{knowledgebaseId}}/access` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-access.md) for the provider-specific parameters and requirements.

