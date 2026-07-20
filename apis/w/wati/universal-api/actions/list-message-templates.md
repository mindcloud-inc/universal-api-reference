# Wati: List Message Templates

Retrieves available message templates from Wati.

```
GET https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-message-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-message-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-message-templates?${params}`, {
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
| `pageSize` | number | no | Number of templates to return per page. Default: `10`. |
| `pageNumber` | number | no | Page number to return. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addSecurityRecommendation": true,
      "body": "string",
      "bodyOriginal": "string",
      "buttons": [
        {}
      ],
      "buttonsType": "string",
      "category": "string",
      "customParams": [
        {}
      ],
      "elementName": "Ava Chen",
      "expiresIn": 1,
      "footer": "string",
      "header": {},
      "hsm": "string",
      "hsmOriginal": "string",
      "id": "string",
      "includeExpiryTime": true,
      "language": {},
      "lastModified": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addSecurityRecommendation` | boolean | Whether security recommendation text is enabled. |
| `body` | string | Rendered template body. |
| `bodyOriginal` | string | Original template body before Wati parameter normalization. |
| `buttons` | array<object> | Button configuration when present. |
| `buttonsType` | string | Button rendering mode. |
| `category` | string | WhatsApp template category. |
| `customParams` | array<object> | Custom parameter definitions when the template uses named parameters. |
| `elementName` | string | Internal Wati template name. |
| `expiresIn` | number | Template expiry interval. |
| `footer` | string | Template footer when present. |
| `header` | object | Header configuration when present. |
| `hsm` | string | Legacy HSM content when present. |
| `hsmOriginal` | string | Original legacy HSM content when present. |
| `id` | string | Wati template identifier. |
| `includeExpiryTime` | boolean | Whether expiry time is included. |
| `language` | object | Template language metadata. |
| `lastModified` | date | When the template was last modified. |
| `status` | string | Template approval status. |
| `type` | string | Wati template record type. |

## Native endpoint

Through the native Wati API, this operation is `GET /api/v1/getMessageTemplates` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-templates.md) for the provider-specific parameters and requirements.

