# Chatling: Get Chatbots Usage

Retrieves chatbot usage from Chatling.

```
GET https://connect.mindcloud.co/v1/universal/chatling/latest/actions/get-chatbots-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/get-chatbots-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatling/latest/actions/get-chatbots-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "max": 1,
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `max` | number | The maximum number of chatbots available to the project. |
| `used` | number | The number of chatbots used by the project. |

## Native endpoint

Through the native Chatling API, this operation is `GET /usage/chatbots` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chatbots-usage.md) for the provider-specific parameters and requirements.

