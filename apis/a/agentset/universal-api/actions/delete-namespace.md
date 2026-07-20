# Agentset: Delete Namespace

Deletes a namespace from Agentset.

```
DELETE https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agentset `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-namespace?connectionId=$CONNECTION_ID&namespaceId=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespaceId": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentset/latest/actions/delete-namespace?${params}`, {
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
| `namespaceId` | string | yes | The Agentset namespace ID, prefixed with ns_. |

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

Through the native Agentset API, this operation is `DELETE /v1/namespace/:namespaceId` (base URL `https://api.agentset.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-namespace.md) for the provider-specific parameters and requirements.

