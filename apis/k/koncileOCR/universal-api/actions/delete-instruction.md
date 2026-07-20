# Koncile OCR: Delete Instruction



```
DELETE https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-instruction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-instruction?connectionId=$CONNECTION_ID&instruction_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instruction_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/delete-instruction?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instruction_id` | string | yes | The instruction identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "instruction_id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `instruction_id` | number | The deleted instruction identifier. |
| `success` | boolean | Whether the delete request succeeded. |

## Native endpoint

Through the native Koncile OCR API, this operation is `DELETE /delete_instruction` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-instruction.md) for the provider-specific parameters and requirements.

