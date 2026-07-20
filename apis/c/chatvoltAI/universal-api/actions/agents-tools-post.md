# Chatvolt AI: Create Tool

Creates a tool in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-tools-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-tools-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-tools-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes |  |
| `type` | string | yes | Type for application/json requests. |
| `datastoreId` | string | no | Required when type is 'datastore'. |
| `formId` | string | no | Required when type is 'form'. |
| `isRaw` | boolean | no | Only applicable when type is 'http'. If true, the tool is configured with a raw cURL command. |
| `config` | object | no | Config for application/json requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "datastoreId": "string",
      "formId": "string",
      "id": "string",
      "isRaw": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object | Config. |
| `datastoreId` | string | Required when type is 'datastore'. |
| `formId` | string | Required when type is 'form'. |
| `id` | string | Id. |
| `isRaw` | boolean | Only applicable when type is 'http'. If true, the tool is configured with a raw cURL command. |
| `type` | string | Type. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /api/agents/{agentId}/tools` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-tools-post.md) for the provider-specific parameters and requirements.

