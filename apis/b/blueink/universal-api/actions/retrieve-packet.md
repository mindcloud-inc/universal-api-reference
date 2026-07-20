# Blueink: Retrieve Packet

Retrieves an existing packet from Blueink.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-packet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-packet?connectionId=$CONNECTION_ID&packetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "packetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-packet?${params}`, {
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
| `packetId` | string | yes | Packet ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authId": true,
      "authSelfie": true,
      "authSms": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "deliverVia": "string",
      "email": "ava@example.com",
      "id": "string",
      "key": "string",
      "lastAccessedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "order": 1,
      "personId": "string",
      "phone": "string",
      "signingCompleteRedirect": "string",
      "status": "string",
      "suppressAll": true,
      "suppressDocsReady": true,
      "suppressReminder": true,
      "suppressSigning": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authId` | boolean |  |
| `authSelfie` | boolean |  |
| `authSms` | boolean |  |
| `completedAt` | date |  |
| `deliverVia` | string |  |
| `email` | string |  |
| `id` | string |  |
| `key` | string |  |
| `lastAccessedAt` | date |  |
| `name` | string |  |
| `order` | number |  |
| `personId` | string |  |
| `phone` | string |  |
| `signingCompleteRedirect` | string |  |
| `status` | string |  |
| `suppressAll` | boolean |  |
| `suppressDocsReady` | boolean |  |
| `suppressReminder` | boolean |  |
| `suppressSigning` | boolean |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /packets/:packetId/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-packet.md) for the provider-specific parameters and requirements.

