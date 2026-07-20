# Linguin AI: Bulk Detect Language



```
POST https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/bulk-detect-language
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linguin AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/bulk-detect-language" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "q[]": "Enter one text per item"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linguinAI/latest/actions/bulk-detect-language', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "q[]": "Enter one text per item"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q[]` | array<string> | yes | The texts to analyze for language detection. Accepts multiple values as an array. Example: `Enter one text per item`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<array> | Detected languages for each submitted text, in request order. |

## Native endpoint

Through the native Linguin AI API, this operation is `POST /v2/bulk_detect/language` (base URL `https://api.linguin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-detect-language.md) for the provider-specific parameters and requirements.

