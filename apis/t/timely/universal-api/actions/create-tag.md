# Timely: Create Tag

Creates a tag in Timely.

```
POST https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "label.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timely/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "label.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | Account ID |
| `label.name` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native Timely API, this operation is `POST /1.1/{account_id}/labels` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

