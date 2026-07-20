# Zoho Assist: Create Unattended Session

Creates an unattended remote session for a Zoho Assist device.

```
POST https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-unattended-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-unattended-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "departmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAssist/latest/actions/create-unattended-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "departmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | Device resource ID to connect to. |
| `departmentId` | string | yes | Department containing the target device. |
| `osName` | string | no | Target operating system for Windows or Linux devices. |
| `userId` | string | no | Logged-on user ID when required by the device OS. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authkey": "string",
      "authtype": "string",
      "isUserPresent": true,
      "sessionKey": "string",
      "technicianUri": "string",
      "viewerid": "string"
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
| `isUserPresent` | boolean |  |
| `sessionKey` | string |  |
| `technicianUri` | string |  |
| `viewerid` | string |  |

## Native endpoint

Through the native Zoho Assist API, this operation is `POST /unattended/:resourceId/connect` (base URL `https://assist.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-unattended-session.md) for the provider-specific parameters and requirements.

