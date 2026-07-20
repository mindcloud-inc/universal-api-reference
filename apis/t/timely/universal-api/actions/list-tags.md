# Timely: List Tags

Retrieves tags from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-tags?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-tags?${params}`, {
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
| `accountId` | number | yes | Account ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of labels to return (default: 10000) |
| `offset` | number | no | Number of labels to skip (default: 0) |
| `filter` | string | no | Filter labels by status: all (default), active, or archived |
| `parentId` | number | no | Filter by parent label ID to get child labels only |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "children": [
        {}
      ],
      "created_at": "string",
      "emoji": "string",
      "external_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "parent_id": "string",
      "sequence": 1,
      "tic": {
        "external_url": "https://example.com",
        "tool_id": "string",
        "uri": "string"
      },
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `children` | array<object> |  |
| `created_at` | string |  |
| `emoji` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `parent_id` | string |  |
| `sequence` | number |  |
| `tic` | object |  |
| `tic.external_url` | string |  |
| `tic.tool_id` | string |  |
| `tic.uri` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/labels` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

