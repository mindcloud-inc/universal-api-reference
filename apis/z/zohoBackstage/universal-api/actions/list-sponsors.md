# Zoho Backstage: List Sponsors



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-sponsors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-sponsors?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-sponsors?${params}`, {
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
      "companyName": "Ava Chen",
      "contact": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "telephone": "string"
      },
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "description": "string",
      "id": "string",
      "index": 1,
      "language": "string",
      "lastModifiedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "sponsorshipType": "string",
      "sponsorshipTypeName": "Ava Chen",
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
| `companyName` | string |  |
| `contact.email` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.telephone` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | string |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `id` | string |  |
| `index` | number |  |
| `language` | string |  |
| `lastModifiedBy.email` | string |  |
| `lastModifiedBy.firstName` | string |  |
| `lastModifiedBy.id` | string |  |
| `lastModifiedTime` | date |  |
| `sponsorshipType` | string |  |
| `sponsorshipTypeName` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/sponsors` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sponsors.md) for the provider-specific parameters and requirements.

