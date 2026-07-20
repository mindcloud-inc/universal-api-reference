# DataForms.io: Get Data Form

Retrieves a data form from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-data-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-data-form?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-data-form?${params}`, {
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
| `formId` | string | yes | The DataForms.io form identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "allowMultipleSubmissions": true,
        "createdAt": "string",
        "headline": "string",
        "id": "string",
        "lockAfterSubmission": true,
        "redirectUrl": "https://example.com",
        "templateId": "string",
        "type": "string",
        "updatedAt": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.allowMultipleSubmissions` | boolean |  |
| `data.createdAt` | string |  |
| `data.headline` | string |  |
| `data.id` | string |  |
| `data.lockAfterSubmission` | boolean |  |
| `data.redirectUrl` | string |  |
| `data.templateId` | string |  |
| `data.type` | string |  |
| `data.updatedAt` | string |  |
| `data.url` | string |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /dataforms/{form_id}` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-form.md) for the provider-specific parameters and requirements.

