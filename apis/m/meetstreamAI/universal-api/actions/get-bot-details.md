# Meetstream AI: Get Bot Details

Retrieves bot details from Meetstream AI.

```
GET https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/get-bot-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meetstream AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/get-bot-details?connectionId=$CONNECTION_ID&botId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/meetstreamAI/latest/actions/get-bot-details?${params}`, {
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
| `botId` | string | yes | The bot identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botDetails": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botDetails` | object | Detailed bot payload returned by Meetstream. |

## Native endpoint

Through the native Meetstream AI API, this operation is `GET /bots/:bot_id/detail` (base URL `https://api.meetstream.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-details.md) for the provider-specific parameters and requirements.

