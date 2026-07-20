# DataForms.io: Get Field

Retrieves a field from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-field?connectionId=$CONNECTION_ID&templateId=templ_example&fieldId=field_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "templ_example",
  "fieldId": "field_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-field?${params}`, {
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
| `templateId` | string | yes | The DataForms.io template identifier. Default: `templ_example`. |
| `fieldId` | string | yes | The DataForms.io field identifier. Default: `field_example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        {
          "data": {
            "required": true,
            "validation": "string"
          },
          "id": "string",
          "label": "string",
          "type": "string"
        }
      ],
      "data": {
        "description": "string",
        "headline": "string"
      },
      "id": "string",
      "label": "string",
      "order": 1,
      "sectionId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children[].data.required` | boolean |  |
| `children[].data.validation` | string |  |
| `children[].id` | string |  |
| `children[].label` | string |  |
| `children[].type` | string |  |
| `data.description` | string |  |
| `data.headline` | string |  |
| `id` | string |  |
| `label` | string |  |
| `order` | number |  |
| `sectionId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /templates/{template_id}/fields/{field_id}` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

