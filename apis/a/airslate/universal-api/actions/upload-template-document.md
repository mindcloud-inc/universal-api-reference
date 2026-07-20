# Airslate: Upload Template Document

Uploads a template document to airSlate.

```
POST https://connect.mindcloud.co/v1/universal/airslate/latest/actions/upload-template-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airslate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airslate/latest/actions/upload-template-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airslate/latest/actions/upload-template-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Airslate API, this operation is `POST /organizations/{organization_id}/templates/{template_id}/documents` (base URL `https://api.airslate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-template-document.md) for the provider-specific parameters and requirements.

