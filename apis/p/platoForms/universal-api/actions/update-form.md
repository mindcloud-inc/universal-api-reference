# PlatoForms: Update Form

Updates an existing form in PlatoForms.

```
PUT https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/update-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/update-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/update-form', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form_identifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form_identifier` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_detection_method": "string",
      "folder_id": "string",
      "form_name": "Ava Chen",
      "form_status": "string",
      "form_type": "string",
      "id": "string",
      "pdf_name": "Ava Chen",
      "pdf_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_detection_method` | string |  |
| `folder_id` | string |  |
| `form_name` | string |  |
| `form_status` | string |  |
| `form_type` | string |  |
| `id` | string |  |
| `pdf_name` | string |  |
| `pdf_url` | string |  |

## Native endpoint

Through the native PlatoForms API, this operation is `PATCH /form/{{form_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-form.md) for the provider-specific parameters and requirements.

