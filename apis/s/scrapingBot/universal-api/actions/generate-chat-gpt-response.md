# ScrapingBot: Generate ChatGPT Response



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/generate-chat-gpt-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/generate-chat-gpt-response?connectionId=$CONNECTION_ID&prompt=Reply%20with%20one%20word%3A%20hello" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "prompt": "Reply with one word: hello"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/generate-chat-gpt-response?${params}`, {
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
| `prompt` | string | yes | Prompt to send to the ChatGPT endpoint. Default: `Reply with one word: hello`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "response": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string |  |
| `response` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /chatgpt` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-chat-gpt-response.md) for the provider-specific parameters and requirements.

