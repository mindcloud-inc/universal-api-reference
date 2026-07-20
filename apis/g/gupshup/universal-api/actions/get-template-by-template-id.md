# Gupshup: Get Template By Template ID

Retrieves a template by template ID from Gupshup.

```
GET https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-template-by-template-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-template-by-template-id?connectionId=$CONNECTION_ID&appId=string&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-template-by-template-id?${params}`, {
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
| `appId` | string | yes | Gupshup app ID. |
| `templateId` | string | yes | Gupshup template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "elementName": "Ava Chen",
      "id": "string",
      "languageCode": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Template category. |
| `elementName` | string | Template element name. |
| `id` | string | Gupshup template ID. |
| `languageCode` | string | Template language code. |
| `status` | string | Template approval/status value. |

## Native endpoint

Through the native Gupshup API, this operation is `GET /wa/app/{app_id}/template/{template_id}` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-by-template-id.md) for the provider-specific parameters and requirements.

