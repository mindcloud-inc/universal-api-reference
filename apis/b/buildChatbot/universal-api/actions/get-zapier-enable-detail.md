# BuildChatbot: Get Zapier Enable Detail

Retrieves Zapier enable details from BuildChatbot.

```
GET https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-zapier-enable-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-zapier-enable-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/get-zapier-enable-detail?${params}`, {
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
      "data": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | boolean | Whether Zapier is enabled. |
| `status` | string | Provider response status. |

## Native endpoint

Through the native BuildChatbot API, this operation is `GET /zapier/enable_details` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zapier-enable-detail.md) for the provider-specific parameters and requirements.

