# TranslatePlus: Translate HTML

Translates HTML content in TranslatePlus while preserving structure.

```
POST https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/translate-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/translate-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string",
  "source": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/translate-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string",
    "source": "string",
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes |  |
| `source` | string | yes |  |
| `target` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `POST /v2/translate/html` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-html.md) for the provider-specific parameters and requirements.

