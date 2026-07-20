# Usedesk: Create Client

Creates a new client in Usedesk.

```
POST https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | New customer name. |
| `note` | string | no | Client note text. |
| `phone` | string | no | Client phone number. |
| `emails[]` | array<string> | no | Email addresses for the new client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client_id": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | number |  |
| `status` | boolean |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /create/client` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

