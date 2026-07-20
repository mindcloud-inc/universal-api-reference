# Fabric: List Comments

Retrieves comments for a resource from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-comments?connectionId=$CONNECTION_ID&resourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/list-comments?${params}`, {
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
| `accessToken` | string | no | Access token for published-resource comments when required. |
| `limit` | number | no | Maximum number of comments to return. |
| `offset` | number | no | Number of comments to skip before returning results. |
| `resourceId` | string | yes | The Fabric resource ID for the comments to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": {
        "comments": {
          "createdAt": "string",
          "id": "string",
          "modifiedAt": "string",
          "text": "string"
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
| `data.comments` | array<object> |  |
| `data.comments.createdAt` | string |  |
| `data.comments.id` | string |  |
| `data.comments.modifiedAt` | string |  |
| `data.comments.text` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/resources/{resourceId}/comments` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

