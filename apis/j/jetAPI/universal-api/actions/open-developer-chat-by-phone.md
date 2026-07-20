# JetAPI: Open Developer Chat By Phone

Retrieves a developer chat link from JetAPI by phone.

```
GET https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/open-developer-chat-by-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/open-developer-chat-by-phone?connectionId=$CONNECTION_ID&customerId=1&hash=string&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "hash": "string",
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/open-developer-chat-by-phone?${params}`, {
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
| `customerId` | number | yes | Customer identifier for the developer chat. |
| `hash` | string | yes | Developer chat hash. |
| `phone` | string | yes | Phone number to open in the developer chat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Raw HTML content returned by the developer chat page. |

## Native endpoint

Through the native JetAPI API, this operation is `GET /developer_chat` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-developer-chat-by-phone.md) for the provider-specific parameters and requirements.

