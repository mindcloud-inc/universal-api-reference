# Zoho Backstage: List Ticket Classes



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-ticket-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-ticket-classes?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-ticket-classes?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "attendMode": 1,
      "attendModeString": "string",
      "currencyCode": "string",
      "description": "string",
      "featured": true,
      "hidden": true,
      "id": "string",
      "language": "string",
      "maximumBuyingLimit": 1,
      "minimumBuyingLimit": 1,
      "name": "Ava Chen",
      "quantity": 1,
      "salesEndDate": "2026-05-07T12:00:00.000Z",
      "salesStartDate": "2026-05-07T12:00:00.000Z",
      "sold": 1,
      "status": 1,
      "statusString": "string",
      "ticketClassType": 1,
      "ticketClassTypeString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `attendMode` | number |  |
| `attendModeString` | string |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `featured` | boolean |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `language` | string |  |
| `maximumBuyingLimit` | number |  |
| `minimumBuyingLimit` | number |  |
| `name` | string |  |
| `quantity` | number |  |
| `salesEndDate` | date |  |
| `salesStartDate` | date |  |
| `sold` | number |  |
| `status` | number |  |
| `statusString` | string |  |
| `ticketClassType` | number |  |
| `ticketClassTypeString` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/ticket_classes` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-classes.md) for the provider-specific parameters and requirements.

