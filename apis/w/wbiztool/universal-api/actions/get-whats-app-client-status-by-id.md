# Wbiztool: Get WhatsApp Client Status By Id

Retrieves a specific WhatsApp client status by ID from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-whats-app-client-status-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-whats-app-client-status-by-id?connectionId=$CONNECTION_ID&whatsappClientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "whatsappClientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-whats-app-client-status-by-id?${params}`, {
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
| `whatsappClientId` | number | yes | WhatsApp client ID to check in the URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /whatsapp/status/{{whatsapp_client_id}}/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whats-app-client-status-by-id.md) for the provider-specific parameters and requirements.

