# Needle: Get Collection Stats

Retrieves statistics for a collection from Needle.

```
GET https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-collection-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Needle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-collection-stats?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/needle/latest/actions/get-collection-stats?${params}`, {
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
| `collectionId` | string | yes | ID of the collection to retrieve statistics for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "characters": 1,
      "chunksCount": 1,
      "dataStats": [
        {
          "bytes": 1,
          "files": 1,
          "status": "string"
        }
      ],
      "users": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `characters` | number |  |
| `chunksCount` | number |  |
| `dataStats` | array<object> |  |
| `dataStats[].bytes` | number |  |
| `dataStats[].files` | number |  |
| `dataStats[].status` | string |  |
| `users` | number |  |

## Native endpoint

Through the native Needle API, this operation is `GET /api/v1/collections/:collectionId/stats` (base URL `https://needle.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-stats.md) for the provider-specific parameters and requirements.

