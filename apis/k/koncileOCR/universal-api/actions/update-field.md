# Koncile OCR: Update Field



```
PUT https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "field_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "field_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `desc` | string | no | Update the field description. |
| `field_id` | number | yes | The field identifier to update. |
| `format` | string | no | Update the field format, such as text. |
| `name` | string | no | Update the field name. |
| `position` | string | no | Update the relative position of the field in the output. |
| `type` | string | no | Update whether the field is General fields or Line fields. |

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

Through the native Koncile OCR API, this operation is `PUT /update_field` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

