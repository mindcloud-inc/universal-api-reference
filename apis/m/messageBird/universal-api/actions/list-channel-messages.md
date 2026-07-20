# MessageBird: List Channel Messages



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-channel-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-channel-messages?connectionId=$CONNECTION_ID&workspaceId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/list-channel-messages?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the channel. |
| `channelId` | string | yes | The Bird channel ID whose messages should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endAt": "2026-05-07T12:00:00.000Z",
      "nextPageToken": "string",
      "results": [
        {}
      ],
      "startAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endAt` | date |  |
| `nextPageToken` | string | The token that can be passed as pageToken in URL to retrieve the next set of results. If missing, no more results to display. |
| `results` | array<object> |  |
| `startAt` | date |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/channels/:channelId/messages` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-messages.md) for the provider-specific parameters and requirements.

