# Trak Qr Automation: Create Partner

Creates a new partner in Trak Qr Automation.

```
POST https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trak Qr Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-partner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "brand": "string",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trakQrAutomation/latest/actions/create-partner', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "brand": "string",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Contact email where the Trak API key will be sent. |
| `brand` | string | yes | User-facing brand name of your product. |
| `description` | string | yes | Description of your integration use case. This is not shown to users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable registration result. The API key is sent by email. |

## Native endpoint

Through the native Trak Qr Automation API, this operation is `POST /events-partners` (base URL `https://backend.trak.codes/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-partner.md) for the provider-specific parameters and requirements.

