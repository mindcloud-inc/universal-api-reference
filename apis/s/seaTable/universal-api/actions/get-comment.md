# SeaTable: Get Comment

Retrieves a comment from a SeaTable base.

```
GET https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-comment?connectionId=$CONNECTION_ID&commentId=158118" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "158118"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-comment?${params}`, {
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
| `commentId` | string | yes | The SeaTable comment ID. Default: `158118`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": "string",
      "comment": "string",
      "createdAt": "string",
      "dtableUuid": "string",
      "id": 1,
      "resolved": 1,
      "rowId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | string |  |
| `comment` | string |  |
| `createdAt` | string |  |
| `dtableUuid` | string |  |
| `id` | number |  |
| `resolved` | number |  |
| `rowId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native SeaTable API, this operation is `GET /api-gateway/api/v2/dtables/:base_uuid/comments/:comment_id/` (base URL `https://cloud.seatable.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-comment.md) for the provider-specific parameters and requirements.

