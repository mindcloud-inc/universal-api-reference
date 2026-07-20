# Landbot: List WhatsApp Templates

Retrieves WhatsApp templates from Landbot.

```
GET https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-whatsapp-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Landbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-whatsapp-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/landbot/latest/actions/list-whatsapp-templates?${params}`, {
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
| `channelId` | number | no | Optional channel ID filter to avoid duplicate templates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "templates": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |
| `templates[]` | array<string> |  |

## Native endpoint

Through the native Landbot API, this operation is `GET /v1/channels/whatsapp/templates/` (base URL `https://api.landbot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whatsapp-templates.md) for the provider-specific parameters and requirements.

