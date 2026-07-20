# ThriveDesk: Add Knowledge Base User



```
POST https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/add-knowledge-base-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/add-knowledge-base-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "knowledgebaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/add-knowledge-base-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "knowledgebaseId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw user payload. |
| `email` | string | User email address when returned. |
| `id` | string | User identifier. |
| `name` | string | User name when returned. |
| `role` | string | User role when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `POST /v1/knowledgebases/{{knowledgebaseId}}/users` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-knowledge-base-user.md) for the provider-specific parameters and requirements.

