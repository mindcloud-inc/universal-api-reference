# Koncile OCR: Get Template



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-template?connectionId=$CONNECTION_ID&template_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "template_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/get-template?${params}`, {
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
| `template_id` | string | yes | The template identifier to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "field_ids": [
        1
      ],
      "folder_id": 1,
      "id": 1,
      "instruction_ids": [
        1
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string | The template description. |
| `field_ids` | array<number> | Field identifiers belonging to the template. |
| `folder_id` | number | The parent folder identifier. |
| `id` | number | The template identifier. |
| `instruction_ids` | array<number> | Instruction identifiers belonging to the template. |
| `name` | string | The template name. |

## Native endpoint

Through the native Koncile OCR API, this operation is `GET /fetch_template` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

