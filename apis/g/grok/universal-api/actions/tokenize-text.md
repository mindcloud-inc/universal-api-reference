# Grok: Tokenize Text

Creates a tokenized representation of text in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/tokenize-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/tokenize-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/tokenize-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Model ID to tokenize with. |
| `text` | string | yes | Text content to tokenize. |
| `user` | string | no | Optional user identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tokenIds": [
        {
          "stringToken": "string",
          "tokenBytes": [
            1
          ],
          "tokenId": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tokenIds` | array<object> | Tokenized representation of the input text. |
| `tokenIds[].stringToken` | string | String form of the token. |
| `tokenIds[].tokenBytes` | array<number> | Raw byte values for the token. |
| `tokenIds[].tokenId` | number | Numeric token identifier. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/tokenize-text` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/tokenize-text.md) for the provider-specific parameters and requirements.

