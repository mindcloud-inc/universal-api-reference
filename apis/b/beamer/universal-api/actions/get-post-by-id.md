# Beamer: Get Post By ID

Retrieves a post from Beamer by ID.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-post-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-post-by-id?connectionId=$CONNECTION_ID&postId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-post-by-id?${params}`, {
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
| `postId` | number | yes | ID of the post to retrieve. |
| `userFirstName` | string | no |  |
| `userLastName` | string | no |  |
| `userEmail` | string | no | Email of the user viewing this post. |
| `userId` | string | no | ID of the user viewing this post. |
| `language` | string | no | Retrieve the post translation in this language. |
| `traceableLinks` | boolean | no | Whether to include traceable links in the post. |
| `ignoreRequestDetails` | boolean | no | Ignore request details used for analytics. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `GET /v0/posts/:postId` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-by-id.md) for the provider-specific parameters and requirements.

