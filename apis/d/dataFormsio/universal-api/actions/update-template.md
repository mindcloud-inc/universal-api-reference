# DataForms.io: Update Template

Updates an existing template in DataForms.io.

```
PUT https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | The DataForms.io template identifier. |
| `name` | string | no | Template name. Maximum 255 characters. |
| `description` | string | no | Template description. Maximum 255 characters. |
| `acronym` | string | no | Template acronym. Maximum 10 characters. |
| `redirectUrl` | string | no | Redirect URL to use after form submission. |
| `layout` | string | no | Template layout mode. One of: `0`, `1`. |
| `confirmSubmit` | boolean | no | Show a confirmation modal before submission. |
| `showHeader` | boolean | no | Show the header on the form page. |

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

Through the native DataForms.io API, this operation is `PUT /templates/{template_id}` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

