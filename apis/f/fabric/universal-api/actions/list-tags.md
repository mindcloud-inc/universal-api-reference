# Fabric: List Tags

Retrieves tags from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-tags?${params}`, {
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
| `limit` | number | no | Maximum number of tags to return. |
| `name` | string | no | Filter tags by name. |
| `offset` | number | no | Number of tags to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": {
        "tags": {
          "createdAt": "string",
          "description": "string",
          "id": "string",
          "modifiedAt": "string",
          "name": "Ava Chen",
          "userId": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | object |  |
| `data.tags` | array<object> |  |
| `data.tags.createdAt` | string |  |
| `data.tags.description` | string |  |
| `data.tags.id` | string |  |
| `data.tags.modifiedAt` | string |  |
| `data.tags.name` | string |  |
| `data.tags.userId` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/tags` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

