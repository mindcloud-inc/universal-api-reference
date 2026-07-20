# Vimeo: List Channels

Retrieves channel records from the Vimeo API.

```
GET https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/list-channels?${params}`, {
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
| `query` | string | no | The search query to use to filter the returned channels. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | list | no | Return only channels that match the selected channel filter. One of: `featured`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "header": {},
      "link": "https://example.com",
      "metadata": {},
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pictures": {},
      "privacy": {},
      "resourceKey": "string",
      "tags": [
        {}
      ],
      "uri": "string",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> | The channel categories. |
| `createdTime` | date | When the channel was created. |
| `description` | string | The channel description, when present. |
| `header` | object | The channel header image object. |
| `link` | string | The public Vimeo URL for the channel. |
| `metadata` | object | The channel metadata connections and interactions. |
| `modifiedTime` | date | When the channel was last modified. |
| `name` | string | The channel name. |
| `pictures` | object | The channel pictures object. |
| `privacy` | object | The channel privacy settings. |
| `resourceKey` | string | The Vimeo resource key for the channel. |
| `tags` | array<object> | The tags associated with the channel. |
| `uri` | string | The channel URI. |
| `user` | object | The channel owner. |

## Native endpoint

Through the native Vimeo API, this operation is `GET /channels` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

