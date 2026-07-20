# TranslatePlus: Batch Translate Text

Translates multiple texts in one TranslatePlus request.

```
POST https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/batch-translate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TranslatePlus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/batch-translate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "texts[]": [
    "string"
  ],
  "source": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/translatePlus/latest/actions/batch-translate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "texts[]": ["string"],
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
| `texts[]` | array<string> | yes |  |
| `source` | string | yes |  |
| `target` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": 1,
      "successful": 1,
      "total": 1,
      "translations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | number |  |
| `successful` | number |  |
| `total` | number |  |
| `translations` | array<object> |  |

## Native endpoint

Through the native TranslatePlus API, this operation is `POST /v2/translate/batch` (base URL `https://api.translateplus.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-translate-text.md) for the provider-specific parameters and requirements.

