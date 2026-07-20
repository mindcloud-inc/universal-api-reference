# GitBook: List Space Files

Retrieves files from a GitBook space.

```
GET https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-space-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-space-files?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/list-space-files?${params}`, {
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
| `computed` | boolean | no |  |
| `metadata` | boolean | no |  |
| `spaceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "dimensions": {
        "height": 1,
        "width": 1
      },
      "downloadURL": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `dimensions.height` | number |  |
| `dimensions.width` | number |  |
| `downloadURL` | string |  |
| `id` | string |  |
| `name` | string |  |
| `size` | number |  |

## Native endpoint

Through the native GitBook API, this operation is `GET /spaces/:spaceId/content/files` (base URL `https://api.gitbook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-space-files.md) for the provider-specific parameters and requirements.

