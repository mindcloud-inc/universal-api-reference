# Instafill: Get Form



```
GET https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instafill/latest/actions/get-form?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_name": "Ava Chen",
      "form_id": "string",
      "form_url": "https://example.com",
      "id": "string",
      "object": "string",
      "processed": true,
      "uploading": true,
      "uploading_completed_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_name` | string |  |
| `form_id` | string |  |
| `form_url` | string |  |
| `id` | string |  |
| `object` | string |  |
| `processed` | boolean |  |
| `uploading` | boolean |  |
| `uploading_completed_at` | string |  |

## Native endpoint

Through the native Instafill API, this operation is `GET /v1/forms/:id` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form.md) for the provider-specific parameters and requirements.

