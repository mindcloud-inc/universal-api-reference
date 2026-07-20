# Instabot: Get Display Settings

Retrieves display settings from Instabot.

```
GET https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-display-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instabot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-display-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instabot/latest/actions/get-display-settings?${params}`, {
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
      "clientLoggingType": "string",
      "closeDelay": 1,
      "statementTypingDelay": 1,
      "typingDelay": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientLoggingType` | string |  |
| `closeDelay` | number |  |
| `statementTypingDelay` | number |  |
| `typingDelay` | number |  |

## Native endpoint

Through the native Instabot API, this operation is `GET /instabot/displaySettings` (base URL `https://api.instabot.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-display-settings.md) for the provider-specific parameters and requirements.

