# Mocean API: Download WhatsApp Rich Media



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/download-whatsapp-rich-media
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/download-whatsapp-rich-media?connectionId=$CONNECTION_ID&mediaId=string&whatsAppSender=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "string",
  "whatsAppSender": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/download-whatsapp-rich-media?${params}`, {
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
| `mediaId` | string | yes | The Mocean media ID to download. |
| `whatsAppSender` | string | yes | Registered WhatsApp Business sender phone number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mocean API API returns.

## Native endpoint

Through the native Mocean API API, this operation is `GET /rest/2/media/whatsapp` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-whatsapp-rich-media.md) for the provider-specific parameters and requirements.

