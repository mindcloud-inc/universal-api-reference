# Salespanel: Retrieve Contact

Retrieves a contact from your Salespanel account.

```
GET https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salespanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/retrieve-contact?${params}`, {
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
| `contactId` | string | yes | The unique ID of the contact to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acquisitionDetails": {
        "landingIpAddress": "string",
        "landingLocation": {
          "country": "string",
          "countryCode": "string"
        },
        "landingUserAgent": {
          "browser": "string",
          "device": "string",
          "deviceOs": "string"
        },
        "source": "string"
      },
      "companyDetails": {
        "category": "string",
        "domain": "string",
        "industry": "string",
        "location": "string",
        "name": "Ava Chen",
        "website": "string"
      },
      "contactId": "string",
      "personDetails": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "gender": "string",
        "lastName": "Chen",
        "location": "string",
        "name": "Ava Chen",
        "organization": "string",
        "title": "string"
      },
      "webActivitySummary": {
        "firstSeen": "2026-05-07T12:00:00.000Z",
        "lastSeen": "2026-05-07T12:00:00.000Z",
        "totalPageVisits": 1,
        "totalWebsiteSessions": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acquisitionDetails.landingIpAddress` | string |  |
| `acquisitionDetails.landingLocation.country` | string |  |
| `acquisitionDetails.landingLocation.countryCode` | string |  |
| `acquisitionDetails.landingUserAgent.browser` | string |  |
| `acquisitionDetails.landingUserAgent.device` | string |  |
| `acquisitionDetails.landingUserAgent.deviceOs` | string |  |
| `acquisitionDetails.source` | string |  |
| `companyDetails.category` | string |  |
| `companyDetails.domain` | string |  |
| `companyDetails.industry` | string |  |
| `companyDetails.location` | string |  |
| `companyDetails.name` | string |  |
| `companyDetails.website` | string |  |
| `contactId` | string |  |
| `personDetails.email` | string |  |
| `personDetails.firstName` | string |  |
| `personDetails.gender` | string |  |
| `personDetails.lastName` | string |  |
| `personDetails.location` | string |  |
| `personDetails.name` | string |  |
| `personDetails.organization` | string |  |
| `personDetails.title` | string |  |
| `webActivitySummary.firstSeen` | date |  |
| `webActivitySummary.lastSeen` | date |  |
| `webActivitySummary.totalPageVisits` | number |  |
| `webActivitySummary.totalWebsiteSessions` | number |  |

## Native endpoint

Through the native Salespanel API, this operation is `GET /contacts/:contact_id/` (base URL `https://salespanel.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

