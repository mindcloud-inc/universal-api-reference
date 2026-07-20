# Inoreader: List Stream Contents

Retrieves contents from a specific Inoreader stream.

```
GET https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-stream-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-stream-contents?connectionId=$CONNECTION_ID&streamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "streamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-stream-contents?${params}`, {
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
| `streamId` | string | yes | URL-encoded stream ID appended to the endpoint path. |
| `maxItems` | number | no | Number of items to return. |
| `order` | string | no | Return newest first by default, or oldest first with o. |
| `startTime` | number | no | Unix timestamp from which to begin fetching items. |
| `excludeTarget` | string | no | Exclude a target stream or state such as the read state. |
| `includeTarget` | string | no | Include only items matching a specific target label or state. |
| `continuation` | string | no | Continuation token from a previous response. |
| `includeAllDirectStreamIds` | boolean | no | Include automatically added folder tags in article categories. |
| `annotations` | boolean | no | Include your annotations for each article. |
| `summaries` | boolean | no | Include Inoreader Intelligence summaries for each article. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "continuation": "string",
      "description": "string",
      "direction": "string",
      "id": "string",
      "items": [
        {}
      ],
      "self": {},
      "title": "string",
      "updated": 1,
      "updatedUsec": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `continuation` | string | Continuation token for the next page when more items are available. |
| `description` | string | Stream description. |
| `direction` | string | Detected text direction for the stream content payload. |
| `id` | string | Stream ID returned by Inoreader. |
| `items` | array<object> | Articles returned for the stream request. |
| `self` | object | Self link metadata for the request. |
| `title` | string | Stream title. |
| `updated` | number | Last stream update time as a Unix timestamp. |
| `updatedUsec` | string | Last stream update time with microsecond precision. |

## Native endpoint

Through the native Inoreader API, this operation is `GET /stream/contents/:streamId` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stream-contents.md) for the provider-specific parameters and requirements.

