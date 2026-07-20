# Zoho Assist: Create Session

Creates a remote support or screen sharing session in Zoho Assist.

```
POST https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-session', {
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
| `customerEmail` | string | no | Customer email to receive the join invitation. |
| `type` | string | no | Session type: rs for remote support, dm for screen sharing, cb for cobrowse. Default: `rs`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authkey": "string",
      "authtype": "string",
      "customerUrl": "https://example.com",
      "sessionId": "string",
      "technicianUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authkey` | string |  |
| `authtype` | string |  |
| `customerUrl` | string |  |
| `sessionId` | string |  |
| `technicianUrl` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `POST /session` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-session.md) for the provider-specific parameters and requirements.

