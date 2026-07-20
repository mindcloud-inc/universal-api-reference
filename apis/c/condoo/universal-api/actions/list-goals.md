# condoo: List Goals

Retrieves goals from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-goals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-goals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-goals?${params}`, {
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
| `search` | string | no | Optional search string. |
| `searchBy` | string | no | Optional search field. Allowed values: name, path, key. |
| `type` | string | no | Optional goal type. Allowed values: pageview, custom. |
| `websiteId` | number | no | Optional website ID selector. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "key": "string",
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "path": "string",
      "type": "string",
      "user_id": 1,
      "website_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date |  |
| `id` | number |  |
| `key` | string |  |
| `last_datetime` | date |  |
| `name` | string |  |
| `path` | string |  |
| `type` | string |  |
| `user_id` | number |  |
| `website_id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `GET /goals/` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-goals.md) for the provider-specific parameters and requirements.

