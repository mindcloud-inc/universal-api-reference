# Weaviate Vector Store: Get Object

Retrieves an object from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-object?connectionId=$CONNECTION_ID&className=Ava%20Chen&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "className": "Ava Chen",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-object?${params}`, {
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
| `className` | string | yes |  |
| `id` | string | yes |  |

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

Through the native Weaviate Vector Store API, this operation is `GET /v1/objects/:className/:id` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-object.md) for the provider-specific parameters and requirements.

