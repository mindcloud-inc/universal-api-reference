# Inoreader: List Folders and Tags

Retrieves folders and tags from Inoreader.

```
GET https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-folders-and-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-folders-and-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/list-folders-and-tags?${params}`, {
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
| `includeTypes` | number | no | Set to 1 to include the tag item type in the response. |
| `includeCounts` | number | no | Set to 1 to include unread and unseen counts for tags and active searches. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags` | array<object> | The tags returned by Inoreader for the connected account. |

## Native endpoint

Through the native Inoreader API, this operation is `GET /tag/list` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders-and-tags.md) for the provider-specific parameters and requirements.

