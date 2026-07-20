# DataForms.io: Update Data Form

Updates an existing data form in DataForms.io.

```
PUT https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/update-data-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/update-data-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/update-data-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | string | yes | The DataForms.io form identifier. |
| `headline` | string | no | The form headline. |
| `allowMultipleSubmissions` | boolean | no | Allow a user to submit the form multiple times. |
| `lockAfterSubmission` | boolean | no | Lock the form after a submission is completed. |
| `redirectUrl` | string | no | Redirect URL to use after form submission. |

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

Through the native DataForms.io API, this operation is `PUT /dataforms/{form_id}` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-form.md) for the provider-specific parameters and requirements.

