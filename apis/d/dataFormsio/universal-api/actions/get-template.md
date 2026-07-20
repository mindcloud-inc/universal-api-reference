# DataForms.io: Get Template

Retrieves a template from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-template?${params}`, {
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
| `templateId` | string | yes | The DataForms.io template identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "acronym": "string",
        "createdAt": "string",
        "description": "string",
        "id": "string",
        "name": "Ava Chen",
        "redirectUrl": "https://example.com",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.acronym` | string |  |
| `data.createdAt` | string |  |
| `data.description` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.redirectUrl` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /templates/{template_id}` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

