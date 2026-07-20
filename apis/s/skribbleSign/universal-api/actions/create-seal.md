# Skribble Sign: Create Seal

Creates a new seal in Skribble Sign.

```
POST https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-seal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-seal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/create-seal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The base64 encoded PDF content to seal. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountName` | string | no | Optional predefined company seal account name. |
| `visualSignature` | object | no | Optional visual seal placement payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "content_type": "string",
      "document_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Sealed document content when returned inline. |
| `content_type` | string | Result MIME type. |
| `document_id` | string | Sealed document ID. |

## Native endpoint

Through the native Skribble Sign API, this operation is `POST /v2/seal` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-seal.md) for the provider-specific parameters and requirements.

