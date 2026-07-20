# Linguin AI: Detect Profanity



```
POST https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/detect-profanity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linguin AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/detect-profanity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "q": "You are a moron!"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/detect-profanity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "q": "You are a moron!"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | yes | The text to analyze for profanity. Example: `You are a moron!`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `score` | number | The profanity score for the submitted text. |

## Native endpoint

Through the native Linguin AI API, this operation is `POST /v2/detect/profanity` (base URL `https://api.linguin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-profanity.md) for the provider-specific parameters and requirements.

