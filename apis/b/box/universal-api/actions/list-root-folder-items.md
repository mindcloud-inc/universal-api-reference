# Box: List Root Folder Items



```
GET https://connect.mindcloud.co/v1/universal/box/latest/actions/list-root-folder-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Box `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/box/latest/actions/list-root-folder-items?connectionId=$CONNECTION_ID&folderId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/box/latest/actions/list-root-folder-items?${params}`, {
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
| `folderId` | string | yes | Root folder ID. This action is preconfigured to use `0`. Default: `0`. Example: `0`. |
| `limit` | number | no | Maximum number of root items to return. Example: `100`. |
| `offset` | number | no | Offset-based pagination start position for root items. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `usemarker` | boolean | no | Set true to use marker-based pagination for root items. Example: `true`. |
| `marker` | string | no | Marker token for the next page of root items. Example: `AAEAAQ...`. |
| `sort` | string | no | Optional secondary sort field for root items. Example: `name`. |
| `direction` | string | no | Sort direction: ASC or DESC. Example: `ASC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "limit": 1,
      "next_marker": "string",
      "offset": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | The root folder items returned for this page. |
| `limit` | number | The page size limit. |
| `next_marker` | string | Marker for the next page when marker pagination is active. |
| `offset` | number | The offset used for this page when offset pagination is active. |
| `total_count` | number | The total number of root items available. |

## Native endpoint

Through the native Box API, this operation is `GET /folders/:folder_id/items` (base URL `https://api.box.com/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-root-folder-items.md) for the provider-specific parameters and requirements.

