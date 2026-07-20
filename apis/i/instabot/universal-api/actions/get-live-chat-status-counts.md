# Instabot: Get Live Chat Status Counts

Retrieves live chat status counts from Instabot.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-live-chat-status-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-live-chat-status-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-live-chat-status-counts?${params}`, {
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
| `searchString` | string | no | Text used to filter chat status counts. |
| `startDate` | date | no | Start of the date window for live chat status counts. |
| `endDate` | date | no | End of the date window for live chat status counts. |
| `botDeletionStatus` | string | no | Filter counts by bot deletion status. Default: `all`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Instabot API returns.

## Native endpoint

Through the native Instabot API, this operation is `POST /instabot/chats/liveChatStatusCounts` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-chat-status-counts.md) for the provider-specific parameters and requirements.

