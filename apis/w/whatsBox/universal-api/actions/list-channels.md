# WhatsBox: List Channels

Retrieves connected WhatsApp phone numbers from WhatsBox.

```
GET https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsBox/latest/actions/list-channels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "channelLabel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "displayPhoneNumber": "string",
      "id": "string",
      "phoneNumber": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string",
      "verifiedName": "Ava Chen",
      "wabaId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelLabel` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `displayPhoneNumber` | string |  |
| `id` | string |  |
| `phoneNumber` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |
| `verifiedName` | string |  |
| `wabaId` | string |  |

## Native endpoint

Through the native WhatsBox API, this operation is `GET /channels` (base URL `https://api.whatsbox.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

