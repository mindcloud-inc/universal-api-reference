# StoryChief: Update Author

Updates an existing author in StoryChief.

```
PUT https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-author" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authorId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-author', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authorId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorId` | number | yes | Author identifier from the path. |
| `bio` | string | no |  |
| `email` | string | no |  |
| `facebookLink` | string | no | Author Facebook profile URL. |
| `firstName` | string | no |  |
| `lastName` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native StoryChief API returns.

## Native endpoint

Through the native StoryChief API, this operation is `PUT /authors/:authorId` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-author.md) for the provider-specific parameters and requirements.

