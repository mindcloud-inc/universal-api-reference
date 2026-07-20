# ActiveCampaign: Create Contact

Creates a new contact in ActiveCampaign.

```
POST https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveCampaign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeCampaign/latest/actions/create-contact', {
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
| `contact` | object | no |  |
| `contact.email` | string | no |  |
| `contact.firstName` | string | no |  |
| `contact.lastName` | string | no |  |
| `contact.phone` | string | no |  |
| `contact.fieldValues[]` | array<object> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact.allowNullEmail` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cdate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "links": {
        "accountContacts": "https://example.com",
        "automationEntryCounts": "https://example.com",
        "bounceLogs": "https://example.com",
        "contactAutomations": "https://example.com",
        "contactData": "https://example.com",
        "contactDeals": "https://example.com",
        "contactGoals": "https://example.com",
        "contactLists": "https://example.com",
        "contactLogs": "https://example.com",
        "contactTags": "https://example.com",
        "deals": "https://example.com",
        "fieldValues": "https://example.com",
        "geoIps": "https://example.com",
        "notes": "https://example.com",
        "organization": "https://example.com",
        "plusAppend": "https://example.com",
        "scoreValues": "https://example.com",
        "trackingLogs": "https://example.com"
      },
      "organization": {},
      "orgid": "string",
      "orgname": "Ava Chen",
      "phone": "string",
      "udate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cdate` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `links.accountContacts` | string |  |
| `links.automationEntryCounts` | string |  |
| `links.bounceLogs` | string |  |
| `links.contactAutomations` | string |  |
| `links.contactData` | string |  |
| `links.contactDeals` | string |  |
| `links.contactGoals` | string |  |
| `links.contactLists` | string |  |
| `links.contactLogs` | string |  |
| `links.contactTags` | string |  |
| `links.deals` | string |  |
| `links.fieldValues` | string |  |
| `links.geoIps` | string |  |
| `links.notes` | string |  |
| `links.organization` | string |  |
| `links.plusAppend` | string |  |
| `links.scoreValues` | string |  |
| `links.trackingLogs` | string |  |
| `organization` | object |  |
| `orgid` | string |  |
| `orgname` | string |  |
| `phone` | string |  |
| `udate` | date |  |

## Native endpoint

Through the native ActiveCampaign API, this operation is `POST /contacts` (base URL `{{credentials.apiUrl}}/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

