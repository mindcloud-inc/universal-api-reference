# Koncile OCR: Update Instruction



```
PUT https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-instruction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-instruction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instruction_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-instruction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instruction_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | Update the instruction text. |
| `instruction_id` | number | yes | The instruction identifier to update. |
| `type` | string | no | Update whether the instruction targets General fields or Line fields. |

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

Through the native Koncile OCR API, this operation is `PUT /update_instruction` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-instruction.md) for the provider-specific parameters and requirements.

