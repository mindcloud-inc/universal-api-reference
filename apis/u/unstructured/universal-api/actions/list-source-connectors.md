# Unstructured: List Source Connectors

Retrieves a list of source connectors from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-source-connectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-source-connectors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/list-source-connectors?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "createdAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `createdAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Unstructured API, this operation is `GET /sources/` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-source-connectors.md) for the provider-specific parameters and requirements.

