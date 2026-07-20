# Timely: Update Tag

Updates an existing tag in Timely.

```
PUT https://connect.mindcloud.co/v1/universal/timely/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timely/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timely/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Account ID |
| `id` | number | yes | Label ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label.name` | string | no |  |
| `label.emoji` | string | no |  |
| `label.parentId` | string | no |  |
| `label.sequence` | string | no |  |
| `label.active` | string | no |  |
| `label.externalId` | string | no |  |

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

Through the native Timely API, this operation is `PUT /1.1/{account_id}/labels/{id}` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

