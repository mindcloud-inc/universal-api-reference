# Koncile OCR: Create Template



```
POST https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folder_id": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folder_id": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date_locale` | string | no | Locale for date formatting, such as EU or US. |
| `desc` | string | no | A description of the template. |
| `folder_id` | number | yes | The folder identifier the template belongs to. |
| `name` | string | yes | The template name to create. |
| `number_locale` | string | no | Locale for number formatting, such as EU or US. |
| `template_id` | number | no | Copy an existing template into the new template when provided. |

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

Through the native Koncile OCR API, this operation is `POST /create_template` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

