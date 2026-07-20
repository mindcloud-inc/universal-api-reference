# Koncile OCR: Get Field



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-field?connectionId=$CONNECTION_ID&field_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-field?${params}`, {
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
| `field_id` | string | yes | The field identifier to fetch. |

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

Through the native Koncile OCR API, this operation is `GET /fetch_field` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

