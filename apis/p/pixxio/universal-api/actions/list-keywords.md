# pixx.io: List Keywords

Retrieves keywords from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-keywords?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/list-keywords?${params}`, {
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
| `exactMatch` | boolean | no | Whether the keyword name filter must match exactly. |
| `name` | string | no | Filter keywords by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keywords": {
        "id": 1,
        "name": "Ava Chen"
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
| `keywords` | array<object> |  |
| `keywords.id` | number |  |
| `keywords.name` | string |  |
| `quantity` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /keywords` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-keywords.md) for the provider-specific parameters and requirements.

