# Gupshup: Create Template

Creates a template in Gupshup.

```
POST https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "languageCode": "string",
  "content": "string",
  "category": "string",
  "elementName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "languageCode": "string",
    "content": "string",
    "category": "string",
    "elementName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Gupshup app ID. |
| `example` | string | no | Template body example values when variables are used. |
| `footer` | string | no | Optional template footer text. |
| `vertical` | string | no | Template vertical or use case label. |
| `languageCode` | string | yes | Valid language code for the template. |
| `content` | string | yes | Template body content. |
| `category` | string | yes | Template category. |
| `elementName` | string | yes | Template name/element name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Gupshup response message. |
| `status` | string | Template creation status returned by Gupshup. |
| `templateId` | string | Created template ID when returned by Gupshup. |

## Native endpoint

Through the native Gupshup API, this operation is `POST /wa/app/{app_id}/template` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

