# Cloro: Extract Google Gemini



```
POST https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-gemini
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-gemini" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloro/latest/actions/extract-google-gemini', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country` | string | no | Country/region code for localized response. |
| `prompt` | string | yes | The prompt to send to Gemini. |
| `include` | object | no | Optional flags for additional response formats. |
| `include.markdown` | boolean | no | Include markdown formatted response content. |
| `include.html` | boolean | no | Include HTML response content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "text": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.text` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloro API, this operation is `POST /v1/monitor/gemini` (base URL `https://api.cloro.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-google-gemini.md) for the provider-specific parameters and requirements.

