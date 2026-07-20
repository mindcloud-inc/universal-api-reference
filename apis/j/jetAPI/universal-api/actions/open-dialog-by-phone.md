# JetAPI: Open Dialog By Phone

Retrieves a chat dialog link from JetAPI by phone.

```
GET https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/open-dialog-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/open-dialog-by-phone?connectionId=$CONNECTION_ID&customerId=1&hash=string&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "hash": "string",
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/open-dialog-by-phone?${params}`, {
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
| `customerId` | number | yes | Unique client ID from the created chat link. |
| `hash` | string | yes | Unique hash returned by Create Chat Link. |
| `phone` | string | yes | Recipient phone number. |
| `dispatchRouting` | string | no | Optional sending channel, whatsapp or tdlib. |
| `chatOnly` | boolean | no | When true, opens an isolated dialog without chat list navigation. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderId` | number | no | Optional sender ID for tdlib dialogs. |
| `username` | string | no | Optional recipient username for tdlib dialogs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string | Direct iframe dialog link for the requested phone. |
| `meta` | object | Response metadata. |

## Native endpoint

Through the native JetAPI API, this operation is `GET /api/v1/chatter/` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-dialog-by-phone.md) for the provider-specific parameters and requirements.

