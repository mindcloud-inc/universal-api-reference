# pixx.io: List Upload Links

Retrieves upload links from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-upload-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-upload-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-upload-links?${params}`, {
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
| `isActive` | boolean | no | Filter upload links by active status. |
| `name` | string | no | Filter upload links by name. |
| `userId` | number | no | Filter upload links by user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "quantity": 1,
      "success": true,
      "uploadLinks": {
        "id": 1,
        "name": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `quantity` | number |  |
| `success` | boolean |  |
| `uploadLinks` | array<object> |  |
| `uploadLinks.id` | number |  |
| `uploadLinks.name` | string |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /uploadLinks` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-upload-links.md) for the provider-specific parameters and requirements.

