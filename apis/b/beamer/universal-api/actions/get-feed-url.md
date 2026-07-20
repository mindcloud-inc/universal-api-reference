# Beamer: Get Feed URL

Retrieves the Beamer feed URL for a user.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-feed-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-feed-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/get-feed-url?${params}`, {
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
| `language` | string | no | Retrieve the feed URL in a specific language. |
| `filterByUrl` | boolean | no | Apply URL filtering to the feed. |
| `filter` | string | no | Retrieve posts with a matching segmentation filter. |
| `forceFilter` | string | no | Only retrieve posts that match this segmentation filter. |
| `userFirstName` | string | no | First name of the user viewing the feed. |
| `userLastName` | string | no | Last name of the user viewing the feed. |
| `userEmail` | string | no | Email of the user viewing the feed. |
| `userId` | string | no | ID of the user viewing the feed. |
| `theme` | string | no | Feed theme to use in the generated URL. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `GET /v0/url` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feed-url.md) for the provider-specific parameters and requirements.

