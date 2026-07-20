# PlatoForms: Create Form

Creates a new form in PlatoForms.

```
POST https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlatoForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form_identifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platoForms/latest/actions/create-form', {
  method: 'POST',
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

Through the native PlatoForms API, this operation is `POST /form/{{form_identifier}}/` (base URL `https://api.platoforms.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-form.md) for the provider-specific parameters and requirements.

