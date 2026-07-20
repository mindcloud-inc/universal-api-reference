# zipBoard: Get Review Links

Retrieves review links from zipBoard.

```
GET https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-review-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-review-links?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-review-links?${params}`, {
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
| `fileId` | string | no | Optional file ID to fetch review links for. |
| `projectId` | string | no | Optional project ID to fetch review links for. |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileId": "string",
      "linkAccess": "https://example.com",
      "linkTokenId": "https://example.com",
      "loginRequired": true,
      "message": "string",
      "projectId": "string",
      "shareLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileId` | string |  |
| `linkAccess` | string |  |
| `linkTokenId` | string |  |
| `loginRequired` | boolean |  |
| `message` | string |  |
| `projectId` | string |  |
| `shareLink` | string |  |

## Native endpoint

Through the native zipBoard API, this operation is `GET /shareurl` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review-links.md) for the provider-specific parameters and requirements.

