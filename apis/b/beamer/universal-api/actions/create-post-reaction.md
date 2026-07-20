# Beamer: Create Post Reaction

Creates a post reaction in Beamer.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/create-post-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/create-post-reaction?connectionId=$CONNECTION_ID&postId=1&reaction=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "1",
  "reaction": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/create-post-reaction?${params}`, {
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
| `postId` | number | yes |  |
| `reaction` | string | yes |  |
| `userId` | string | no |  |
| `userEmail` | string | no |  |
| `userFirstname` | string | no |  |
| `userLastname` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `POST /v0/posts/:postId/reactions` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post-reaction.md) for the provider-specific parameters and requirements.

