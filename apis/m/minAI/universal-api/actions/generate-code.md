# 1minAI: Generate code

Creates code from a prompt in 1minAI.

```
POST https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1minAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/generate-code', {
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
| `prompt` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webSearch` | boolean | no |  |
| `numOfSite` | number | no | Default: `3`. |
| `maxWord` | number | no | Default: `1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiRecord": {},
      "temporaryUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiRecord` | object |  |
| `temporaryUrl` | string |  |

## Native endpoint

Through the native 1minAI API, this operation is `POST /api/features` (base URL `https://api.1min.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-code.md) for the provider-specific parameters and requirements.

