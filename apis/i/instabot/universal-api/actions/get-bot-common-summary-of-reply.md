# Instabot: Get Bot Common Summary Of Reply

Retrieves a bot reply summary from Instabot.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-bot-common-summary-of-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-bot-common-summary-of-reply?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-bot-common-summary-of-reply?${params}`, {
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
| `id` | number | yes | Instabot bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "engagedCount": 1,
      "goalCompletionsCount": 1,
      "sessionCount": 1,
      "userCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `engagedCount` | number |  |
| `goalCompletionsCount` | number |  |
| `sessionCount` | number |  |
| `userCount` | number |  |

## Native endpoint

Through the native Instabot API, this operation is `GET /instabot/bots/:id/commonSummaryOfReply` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-common-summary-of-reply.md) for the provider-specific parameters and requirements.

