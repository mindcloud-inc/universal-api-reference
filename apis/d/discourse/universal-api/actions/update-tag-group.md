# Discourse: Update Tag Group

Updates an existing tag group in Discourse.

```
PUT https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-tag-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-tag-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-tag-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Tag group id. |
| `one_per_topic` | boolean | no | Whether only one tag from the group can be used per topic. |
| `parent_tag_name` | string | no | Optional parent tag name for the group. |
| `permissions` | string | no | Optional tag group permissions map. |
| `tag_names` | string | no | List of tags that belong to the tag group. |
| `name` | string | yes | Updated name for the Discourse tag group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string",
      "tag_group": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string |  |
| `tag_group` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `PUT /tag_groups/:id.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag-group.md) for the provider-specific parameters and requirements.

