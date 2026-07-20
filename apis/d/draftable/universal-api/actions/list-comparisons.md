# Draftable: List Comparisons

Retrieves your document comparisons from Draftable.

```
GET https://connect.mindcloud.co/v1/universal/draftable/latest/actions/list-comparisons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Draftable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/list-comparisons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/draftable/latest/actions/list-comparisons?${params}`, {
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
      "comparisonType": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "failed": true,
      "identifier": "string",
      "left": {
        "fileType": "string",
        "pageCount": 1,
        "sourceUrl": "https://example.com"
      },
      "public": true,
      "ready": true,
      "readyTime": "2026-05-07T12:00:00.000Z",
      "right": {
        "fileType": "string",
        "pageCount": 1,
        "sourceUrl": "https://example.com"
      },
      "viewerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparisonType` | string |  |
| `creationTime` | date |  |
| `failed` | boolean |  |
| `identifier` | string |  |
| `left.fileType` | string |  |
| `left.pageCount` | number |  |
| `left.sourceUrl` | string |  |
| `public` | boolean |  |
| `ready` | boolean |  |
| `readyTime` | date |  |
| `right.fileType` | string |  |
| `right.pageCount` | number |  |
| `right.sourceUrl` | string |  |
| `viewerUrl` | string |  |

## Native endpoint

Through the native Draftable API, this operation is `GET /comparisons` (base URL `https://api.draftable.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comparisons.md) for the provider-specific parameters and requirements.

