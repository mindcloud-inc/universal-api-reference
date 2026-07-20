# StoryChief: Update Tag

Updates an existing tag in StoryChief.

```
PUT https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tagId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tagId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Updated tag name. |
| `tagId` | number | yes | Tag identifier from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native StoryChief API returns.

## Native endpoint

Through the native StoryChief API, this operation is `PUT /tags/:tagId` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

