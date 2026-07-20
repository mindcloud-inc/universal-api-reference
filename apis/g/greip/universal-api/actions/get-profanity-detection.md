# Greip - Fraud Prevention: Get Profanity Detection

Detects profanity in text with Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-profanity-detection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-profanity-detection?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-profanity-detection?${params}`, {
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
| `text` | string | yes | The text to analyze for profanity or abusive language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isML": true,
      "isSafe": true,
      "riskScore": 1,
      "text": "string",
      "totalBadWords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isML` | boolean |  |
| `isSafe` | boolean |  |
| `riskScore` | number |  |
| `text` | string |  |
| `totalBadWords` | number |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /scoring/profanity` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profanity-detection.md) for the provider-specific parameters and requirements.

