# Teyuto: Update Tag

Updates an existing tag in Teyuto.

```
PUT https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teyuto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": "string",
  "title": "string",
  "hidden": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teyuto/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": "string",
    "title": "string",
    "hidden": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tagId` | string | yes | The Teyuto tag ID to update. |
| `title` | string | yes | Updated title of the tag. |
| `hidden` | boolean | yes | Whether the tag should be hidden. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Teyuto API returns.

## Native endpoint

Through the native Teyuto API, this operation is `PATCH /tags/:tag_id` (base URL `https://api.teyuto.tv/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

