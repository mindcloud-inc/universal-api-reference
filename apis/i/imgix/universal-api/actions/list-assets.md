# imgix: List Assets

Retrieves assets from an imgix source.

```
GET https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-assets?connectionId=$CONNECTION_ID&sourceId=69de49d580720625c04f9162" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "69de49d580720625c04f9162"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-assets?${params}`, {
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
| `cursor` | string | no | Cursor value for the next asset page. |
| `limit` | number | no | Number of assets to return per page. Default: `20`. |
| `sourceId` | string | yes | The imgix source_id. Default: `69de49d580720625c04f9162`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "contentType": "string",
            "fileSize": 1,
            "mediaHeight": 1,
            "mediaKind": "string",
            "mediaWidth": 1,
            "originPath": "string",
            "sourceId": "string"
          },
          "id": "string",
          "type": "string"
        }
      ],
      "meta": {
        "cursor": {
          "current": "string",
          "hasMore": true,
          "totalRecords": "string"
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
| `data[].attributes.contentType` | string |  |
| `data[].attributes.fileSize` | number |  |
| `data[].attributes.mediaHeight` | number |  |
| `data[].attributes.mediaKind` | string |  |
| `data[].attributes.mediaWidth` | number |  |
| `data[].attributes.originPath` | string |  |
| `data[].attributes.sourceId` | string |  |
| `data[].id` | string |  |
| `data[].type` | string |  |
| `meta.cursor.current` | string |  |
| `meta.cursor.hasMore` | boolean |  |
| `meta.cursor.totalRecords` | string |  |

## Native endpoint

Through the native imgix API, this operation is `GET sources/:sourceId/assets` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

