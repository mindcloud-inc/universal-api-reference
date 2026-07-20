# Gupshup: Create Template With Buttons

Creates a template with buttons in Gupshup.

```
POST https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template-with-buttons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template-with-buttons" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/create-template-with-buttons', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Gupshup app ID. |
| `languageCode` | string | no | Valid language code for the template. |
| `content` | string | yes | Template body content. |
| `buttons` | object | no | Template button configuration. |

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

Through the native Gupshup API, this operation is `POST /wa/app/{app_id}/template` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template-with-buttons.md) for the provider-specific parameters and requirements.

