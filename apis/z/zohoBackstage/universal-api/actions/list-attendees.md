# Zoho Backstage: List Attendees



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-attendees?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-attendees?${params}`, {
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
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `eventId` | string | yes | The Zoho Backstage event ID. |
| `ticketId` | string | no | Filter attendees by ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateName": "Ava Chen",
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobileNo": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "eventId": "string",
      "id": "string",
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "orderId": "string",
      "portal": "string",
      "promoCode": "string",
      "purchasedBy": "string",
      "status": 1,
      "statusString": "string",
      "ticketClassId": "string",
      "ticketId": "string",
      "ticketName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateName` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.mobileNo` | string |  |
| `createdTime` | date |  |
| `eventId` | string |  |
| `id` | string |  |
| `lastModifiedTime` | date |  |
| `orderId` | string |  |
| `portal` | string |  |
| `promoCode` | string |  |
| `purchasedBy` | string |  |
| `status` | number |  |
| `statusString` | string |  |
| `ticketClassId` | string |  |
| `ticketId` | string |  |
| `ticketName` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/attendees` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attendees.md) for the provider-specific parameters and requirements.

