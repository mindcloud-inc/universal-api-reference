# Weavely: Generate Form

Creates a generated form in Weavely from a prompt.

```
POST https://connect.mindcloud.co/v1/universal/weavely/latest/actions/generate-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weavely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weavely/latest/actions/generate-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weavely/latest/actions/generate-form', {
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
| `name` | string | no | A friendly name for the form. |
| `prompt` | string | yes | A natural-language description of the form to generate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files[]` | array<object> | no | Optional files as an array of objects with mimeType and base64-encoded data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `url` | string | The URL that opens the generated form in the Weavely editor. |

## Native endpoint

Through the native Weavely API, this operation is `POST /forms/generate` (base URL `https://api.weavely.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-form.md) for the provider-specific parameters and requirements.

