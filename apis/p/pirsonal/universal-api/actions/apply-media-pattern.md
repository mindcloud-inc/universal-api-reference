# Pirsonal: Apply Media Pattern

Applies a pattern to existing media in Pirsonal.

```
PUT https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/apply-media-pattern
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/apply-media-pattern" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaID": "string",
  "patter": "audiolevel",
  "action": "info",
  "parameters": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/apply-media-pattern', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaID": "string",
    "patter": "audiolevel",
    "action": "info",
    "parameters": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaID` | string | yes | ID of the media to transform. |
| `patter` | list<string> | yes | Pattern type. Pirsonal docs list `audiolevel`. One of: `audiolevel`. |
| `action` | list<string> | yes | Pattern action: info, one, or multi. One of: `info`, `multi`, `one`. |
| `parameters` | string | yes | Stringified JSON parameters for the selected pattern, for example an audiolevel threshold object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Pirsonal pattern application response, normally OK or a JSON error string. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-media-pattern.md) for the provider-specific parameters and requirements.

