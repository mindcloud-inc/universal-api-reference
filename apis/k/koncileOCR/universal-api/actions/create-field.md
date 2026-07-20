# Koncile OCR: Create Field



```
POST https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "format": "text",
  "name": "Ava Chen",
  "template_id": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "format": "text",
    "name": "Ava Chen",
    "template_id": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | yes | The field format to extract. Koncile currently requires this value; use text unless a specific format is needed. Default: `text`. |
| `name` | string | yes | The field name to create. |
| `template_id` | number | yes | The template identifier the field belongs to. |
| `type` | string | yes | Whether the field is extracted once (General fields) or for every line (Line fields). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "format": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
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
| `desc` | string | The field description. |
| `format` | string | The field format. |
| `id` | number | The field identifier. |
| `name` | string | The field name. |
| `position` | number | The field position. |
| `template_id` | number | The parent template identifier. |
| `type` | string | Whether the field is General fields or Line fields. |

## Native endpoint

Through the native Koncile OCR API, this operation is `POST /create_field` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

