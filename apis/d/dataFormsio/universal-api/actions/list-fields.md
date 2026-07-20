# DataForms.io: List Fields

Retrieves fields from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-fields?connectionId=$CONNECTION_ID&templateId=templ_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "templ_example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-fields?${params}`, {
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
| `search` | string | no | Filter fields by search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "data": {
            "description": "string",
            "headline": "string",
            "label": "string",
            "required": true,
            "validation": "string"
          },
          "id": "string",
          "label": "string",
          "order": 1,
          "sectionId": "string",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].data.description` | string |  |
| `data[].data.headline` | string |  |
| `data[].data.label` | string |  |
| `data[].data.required` | boolean |  |
| `data[].data.validation` | string |  |
| `data[].id` | string |  |
| `data[].label` | string |  |
| `data[].order` | number |  |
| `data[].sectionId` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /templates/{template_id}/fields` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

