# StoryChief: Get Story Destination Webhook Payload

Retrieves a story destination webhook payload from StoryChief.

```
GET https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-story-destination-webhook-payload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-story-destination-webhook-payload?connectionId=$CONNECTION_ID&destinationId=1&storyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "destinationId": "1",
  "storyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-story-destination-webhook-payload?${params}`, {
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
| `destinationId` | number | yes | Destination identifier from the path. |
| `storyId` | number | yes | Story identifier from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native StoryChief API returns.

## Native endpoint

Through the native StoryChief API, this operation is `GET /stories/:storyId/destinations/:destinationId/webhook` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-story-destination-webhook-payload.md) for the provider-specific parameters and requirements.

