# Weaviate Vector Store: Replace Object

Updates an object in Weaviate.

```
PUT https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/replace-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/replace-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "objectId": "string",
  "className": "Ava Chen",
  "properties.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/replace-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "objectId": "string",
    "className": "Ava Chen",
    "properties.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `classFilter` | string | no |  |
| `objectId` | string | yes |  |
| `className` | string | yes |  |
| `properties.title` | string | yes |  |
| `properties.status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "creationTimeUnix": 1,
      "id": "string",
      "lastUpdateTimeUnix": 1,
      "properties": {
        "status": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `creationTimeUnix` | number |  |
| `id` | string |  |
| `lastUpdateTimeUnix` | number |  |
| `properties.status` | string |  |
| `properties.title` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `PUT /v1/objects/:id` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-object.md) for the provider-specific parameters and requirements.

