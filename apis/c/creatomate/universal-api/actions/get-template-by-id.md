# Creatomate: Get Template By ID

Retrieves a template from Creatomate.

```
GET https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-template-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-template-by-id?connectionId=$CONNECTION_ID&templateId=0bb2ceb3-50b5-48f0-9fe2-84e6bcba43c0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "0bb2ceb3-50b5-48f0-9fe2-84e6bcba43c0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-template-by-id?${params}`, {
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
| `templateId` | string | yes | The ID of the template to retrieve. Example: `0bb2ceb3-50b5-48f0-9fe2-84e6bcba43c0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "source": {},
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `source` | object |  |
| `tags` | array<string> |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Creatomate API, this operation is `GET /v1/templates/:template_id` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-by-id.md) for the provider-specific parameters and requirements.

