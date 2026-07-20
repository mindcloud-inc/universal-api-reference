# Clio Grow: Create Inbox Lead



```
POST https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-inbox-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Grow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-inbox-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "fromMessage": "string",
  "referringUrl": "https://example.com",
  "fromSource": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clioGrow/latest/actions/create-inbox-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "fromMessage": "string",
    "referringUrl": "https://example.com",
    "fromSource": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | First name of the lead. |
| `lastName` | string | yes | Last name of the lead. |
| `fromMessage` | string | yes | Message content from the lead. |
| `referringUrl` | string | yes | URL the lead came from. |
| `fromSource` | string | yes | Source of the lead. |
| `email` | string | no | Email address of the lead. |
| `phoneNumber` | string | no | Phone number of the lead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fromMessage": "string",
      "fromSource": "string",
      "id": 1,
      "lastName": "Chen",
      "phoneNumber": "string",
      "referringUrl": "https://example.com",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `fromMessage` | string |  |
| `fromSource` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phoneNumber` | string |  |
| `referringUrl` | string |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Clio Grow API, this operation is `POST /inbox_leads` (base URL `https://api.clio.com/grow`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inbox-lead.md) for the provider-specific parameters and requirements.

