# pixx.io: List Direct Links

Retrieves direct links from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-direct-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-direct-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-direct-links?${params}`, {
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
| `fileIds` | number<number> | no | Filter direct links by file IDs. Accepts multiple values as an array. |
| `fileName` | string | no | Filter direct links by file name. |
| `isCustom` | boolean | no | Filter by custom direct links. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directLinks": {
        "fileName": "https://example.com",
        "id": 1
      },
      "quantity": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directLinks` | array<object> |  |
| `directLinks.fileName` | string |  |
| `directLinks.id` | number |  |
| `quantity` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /directLinks` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-direct-links.md) for the provider-specific parameters and requirements.

