# Koncile OCR: Create Instruction



```
POST https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-instruction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-instruction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "template_id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-instruction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "template_id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | The instruction text. |
| `template_id` | string | yes | The template identifier the instruction belongs to. |
| `type` | string | yes | Whether the instruction targets General fields or Line fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "id": 1,
      "template_id": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | The instruction text. |
| `id` | number | The instruction identifier. |
| `template_id` | number | The parent template identifier. |
| `type` | string | Whether the instruction targets General fields or Line fields. |

## Native endpoint

Through the native Koncile OCR API, this operation is `POST /create_instruction` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-instruction.md) for the provider-specific parameters and requirements.

