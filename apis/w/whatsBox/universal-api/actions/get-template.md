# WhatsBox: Get Template

Retrieves a WhatsApp template from WhatsBox.

```
GET https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/get-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/get-template?${params}`, {
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
| `id` | string | yes | Template ID. |
| `type` | string | no | Template type. |
| `name` | string | no | Template name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "wabaId": "string",
      "waId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `wabaId` | string |  |
| `waId` | string |  |

## Native endpoint

Through the native WhatsBox API, this operation is `GET /templates/:id` (base URL `https://api.whatsbox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

