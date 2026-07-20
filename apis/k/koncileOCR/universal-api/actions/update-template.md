# Koncile OCR: Update Template



```
PUT https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date_locale` | string | no | Update the date formatting locale. |
| `desc` | string | no | Update the template description. |
| `name` | string | no | Update the template name. |
| `number_locale` | string | no | Update the number formatting locale. |
| `template_id` | number | yes | The template identifier to update. |

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

Through the native Koncile OCR API, this operation is `PUT /update_template` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

