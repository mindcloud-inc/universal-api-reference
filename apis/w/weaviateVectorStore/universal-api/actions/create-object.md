# Weaviate Vector Store: Create Object

Creates an object in Weaviate.

```
POST https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/create-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/create-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "className": "Ava Chen",
  "properties.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/create-object', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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

Through the native Weaviate Vector Store API, this operation is `POST /v1/objects` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-object.md) for the provider-specific parameters and requirements.

