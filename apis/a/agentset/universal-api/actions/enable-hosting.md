# Agentset: Enable Hosting

Enables hosting for an Agentset namespace.

```
POST https://connect.mindcloud.co/v1/universal/agentset/latest/actions/enable-hosting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/enable-hosting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespaceId": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentset/latest/actions/enable-hosting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "namespaceId": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "allowedEmailDomains": [
          "ava@example.com"
        ],
        "allowedEmails": [
          "ava@example.com"
        ],
        "citationMetadataPath": "string",
        "createdAt": "string",
        "exampleQuestions": [
          "string"
        ],
        "exampleSearchQueries": [
          "string"
        ],
        "llmConfig": {},
        "logo": "string",
        "namespaceId": "Ava Chen",
        "ogDescription": "string",
        "ogImage": "string",
        "ogTitle": "string",
        "protected": true,
        "rerankConfig": {},
        "searchEnabled": true,
        "slug": "string",
        "systemPrompt": "string",
        "title": "string",
        "topK": 1,
        "updatedAt": "string",
        "welcomeMessage": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.allowedEmailDomains` | array<string> |  |
| `data.allowedEmails` | array<string> |  |
| `data.citationMetadataPath` | string |  |
| `data.createdAt` | string |  |
| `data.exampleQuestions` | array<string> |  |
| `data.exampleSearchQueries` | array<string> |  |
| `data.llmConfig` | object |  |
| `data.logo` | string |  |
| `data.namespaceId` | string |  |
| `data.ogDescription` | string |  |
| `data.ogImage` | string |  |
| `data.ogTitle` | string |  |
| `data.protected` | boolean |  |
| `data.rerankConfig` | object |  |
| `data.searchEnabled` | boolean |  |
| `data.slug` | string |  |
| `data.systemPrompt` | string |  |
| `data.title` | string |  |
| `data.topK` | number |  |
| `data.updatedAt` | string |  |
| `data.welcomeMessage` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `POST /v1/namespace/:namespaceId/hosting` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enable-hosting.md) for the provider-specific parameters and requirements.

