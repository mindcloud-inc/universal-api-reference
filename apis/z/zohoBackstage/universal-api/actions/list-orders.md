# Zoho Backstage: List Orders



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-orders?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-orders?${params}`, {
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
| `page` | number | no | Page number for paginated order results. |
| `perPage` | number | no | Maximum number of orders to return per page. |
| `orderBy` | string | no | Field used to sort orders. |
| `sortOrder` | string | no | Sort direction for the order list. |
| `status` | string | no | Filter orders by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingAddress": {
        "city": "string",
        "country": "string",
        "name": "Ava Chen",
        "state": "string",
        "streetAddress1": "string",
        "streetAddress2": "string",
        "zipcode": "string"
      },
      "contact": {
        "purchaserEmail": "ava@example.com",
        "purchaserFirstName": "Ava",
        "purchaserLastName": "Chen",
        "purchaserMobileNo": "string"
      },
      "cost": {
        "total": 1
      },
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastModifiedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "orderBy": "string",
      "origin": 1,
      "originString": "string",
      "paymentOptionName": "Ava Chen",
      "paymentStatus": 1,
      "paymentStatusString": "string",
      "paymentType": 1,
      "paymentTypeString": "string",
      "refundPolicy": 1,
      "source": 1,
      "sourceString": "string",
      "status": 1,
      "statusString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.name` | string |  |
| `billingAddress.state` | string |  |
| `billingAddress.streetAddress1` | string |  |
| `billingAddress.streetAddress2` | string |  |
| `billingAddress.zipcode` | string |  |
| `contact.purchaserEmail` | string |  |
| `contact.purchaserFirstName` | string |  |
| `contact.purchaserLastName` | string |  |
| `contact.purchaserMobileNo` | string |  |
| `cost.total` | number |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | string |  |
| `createdTime` | date |  |
| `id` | string |  |
| `lastModifiedBy.email` | string |  |
| `lastModifiedBy.firstName` | string |  |
| `lastModifiedBy.id` | string |  |
| `lastModifiedTime` | date |  |
| `orderBy` | string |  |
| `origin` | number |  |
| `originString` | string |  |
| `paymentOptionName` | string |  |
| `paymentStatus` | number |  |
| `paymentStatusString` | string |  |
| `paymentType` | number |  |
| `paymentTypeString` | string |  |
| `refundPolicy` | number |  |
| `source` | number |  |
| `sourceString` | string |  |
| `status` | number |  |
| `statusString` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/orders` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

