# Agentset: Update Namespace

Updates an existing namespace in Agentset.

```
PUT https://connect.mindcloud.co/v1/universal/agentset/latest/actions/update-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/update-namespace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "namespaceId": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agentset/latest/actions/update-namespace', {
  method: 'PUT',
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
| `name` | string | no | The updated namespace name. |
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |
| `slug` | string | no | The updated namespace slug. |

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

Through the native Agentset API, this operation is `PATCH /v1/namespace/:namespaceId` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-namespace.md) for the provider-specific parameters and requirements.

