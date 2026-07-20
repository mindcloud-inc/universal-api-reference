# StoryChief: Delete Author

Deletes an author from StoryChief.

```
DELETE https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/delete-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/delete-author?connectionId=$CONNECTION_ID&authorId=1&replacementAuthorId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorId": "1",
  "replacementAuthorId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/delete-author?${params}`, {
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
| `authorId` | number | yes | Author identifier from the path. |
| `replacementAuthorId` | number | yes | Replacement author ID documented for deleting an author. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native StoryChief API returns.

## Native endpoint

Through the native StoryChief API, this operation is `DELETE /authors/:authorId` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-author.md) for the provider-specific parameters and requirements.

