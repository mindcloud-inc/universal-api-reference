# StoryChief: Create Author

Creates a new author in StoryChief.

```
POST https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-author" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-author', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bio` | string | no | Author biography. |
| `email` | string | no | Author email address. |
| `firstName` | string | no | Author first name. |
| `lastName` | string | no | Author last name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native StoryChief API returns.

## Native endpoint

Through the native StoryChief API, this operation is `POST /authors` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-author.md) for the provider-specific parameters and requirements.

