# GPTBots: Get Agent Information

Retrieves the configured agent information from GPTBots.

```
GET https://connect.mindcloud.co/v1/universal/gPTBots/latest/actions/get-agent-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GPTBots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gPTBots/latest/actions/get-agent-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gPTBots/latest/actions/get-agent-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GPTBots API returns.

## Native endpoint

Through the native GPTBots API, this operation is `GET /v1/bot/detail` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-information.md) for the provider-specific parameters and requirements.

