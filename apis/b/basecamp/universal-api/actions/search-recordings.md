# Basecamp: Search Recordings

Finds recordings in Basecamp by search query.

```
GET https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/search-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/search-recordings?connectionId=$CONNECTION_ID&accountId=6172410&q=authentication" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "6172410",
  "q": "authentication"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/search-recordings?${params}`, {
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
| `accountId` | string | yes | Basecamp account ID. Example: `6172410`. |
| `q` | string | yes | Search query string. Example: `authentication`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Filter by recording type. Example: `Message`. |
| `bucketId` | number | no | Filter by project ID. Example: `46425319`. |
| `creatorId` | number | no | Filter by creator person ID. Example: `51951159`. |
| `fileType` | string | no | Filter attachments by file type. Example: `PDF`. |
| `excludeChat` | string | no | Exclude chat results when set. Example: `1`. |
| `page` | number | no | Page number for pagination. Example: `1`. |
| `perPage` | number | no | Number of results per page. Example: `50`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `GET /:accountId/search.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recordings.md) for the provider-specific parameters and requirements.

