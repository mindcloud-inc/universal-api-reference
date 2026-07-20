# Salespanel: List Leads

Retrieves leads from your Salespanel account.

```
GET https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salespanel `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-leads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salespanel/latest/actions/list-leads?${params}`, {
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
| `selectByFirstActivity` | boolean | no | Retrieve leads based on first activity instead of most recent activity. Default: `false`. |

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

Through the native Salespanel API, this operation is `GET /leads/` (base URL `https://salespanel.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leads.md) for the provider-specific parameters and requirements.

