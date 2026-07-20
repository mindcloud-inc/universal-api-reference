# Zoho Backstage: List Exhibitors



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-exhibitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-exhibitors?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-exhibitors?${params}`, {
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
      "boothId": "string",
      "companyName": "Ava Chen",
      "companyOverview": "string",
      "companyShortDescription": "string",
      "companySocialPages": {
        "facebook": "string"
      },
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "mobileNo": "string"
      },
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "lastModifiedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `boothId` | string |  |
| `companyName` | string |  |
| `companyOverview` | string |  |
| `companyShortDescription` | string |  |
| `companySocialPages.facebook` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.mobileNo` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `lastModifiedBy.email` | string |  |
| `lastModifiedBy.firstName` | string |  |
| `lastModifiedBy.id` | string |  |
| `lastModifiedTime` | date |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/exhibitors` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-exhibitors.md) for the provider-specific parameters and requirements.

