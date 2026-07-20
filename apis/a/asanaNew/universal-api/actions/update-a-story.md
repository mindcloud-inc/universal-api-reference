# Asana: Update a story

Updates a story in Asana.

```
PUT https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "string",
  "storyGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-story', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "string",
    "storyGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes |  |
| `storyGid` | string | yes | Asana story gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `opt_fields` | list<string> | no | Asana opt fields parameter. |
| `data.gid` | string | no | Asana gid parameter. |
| `data.resource_type` | string | no | Asana resource type parameter. |
| `data.created_at` | string | no | Asana created at parameter. |
| `data.resource_subtype` | string | no | Asana resource subtype parameter. |
| `data.text` | string | no | Asana text parameter. |
| `data.html_text` | string | no | Asana html text parameter. |
| `data.is_pinned` | boolean | no | Asana is pinned parameter. |
| `data.sticker_name` | string | no | Asana sticker name parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `PUT stories/:story_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-story.md) for the provider-specific parameters and requirements.

