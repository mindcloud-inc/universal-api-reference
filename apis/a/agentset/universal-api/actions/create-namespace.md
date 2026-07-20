# Agentset: Create Namespace

Creates a new namespace in Agentset.

```
POST https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-namespace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentset/latest/actions/create-namespace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The namespace name. |
| `slug` | string | yes | A URL-safe namespace slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "embeddingConfig": {},
        "id": "string",
        "name": "Ava Chen",
        "organizationId": "string",
        "slug": "string",
        "vectorStoreConfig": {}
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
| `data.createdAt` | string |  |
| `data.embeddingConfig` | object |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.organizationId` | string |  |
| `data.slug` | string |  |
| `data.vectorStoreConfig` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Agentset API, this operation is `POST /v1/namespace` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-namespace.md) for the provider-specific parameters and requirements.

