# People Data Labs: Search Companies



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/search-companies?connectionId=$CONNECTION_ID&limit=25&offset=0&sql=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sql": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/search-companies?${params}`, {
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
| `sql` | string | yes | People Data Labs company search SQL clause in the form SELECT * FROM company WHERE ... |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliatedProfiles": [
        [
          "string"
        ]
      ],
      "alternativeDomains": [
        [
          "string"
        ]
      ],
      "alternativeNames": [
        [
          "Ava Chen"
        ]
      ],
      "datasetVersion": "string",
      "displayName": "Ava Chen",
      "employeeCount": 1,
      "facebookUrl": "https://example.com",
      "founded": 1,
      "fundingStages": [
        [
          "string"
        ]
      ],
      "headline": "string",
      "id": "string",
      "industry": "string",
      "industryV2": "string",
      "lastFundingDate": "2026-05-07T12:00:00.000Z",
      "latestFundingStage": "string",
      "linkedinId": "https://example.com",
      "linkedinSlug": "https://example.com",
      "linkedinUrl": "https://example.com",
      "location": {
        "addressLine2": "string",
        "continent": "string",
        "country": "string",
        "geo": "string",
        "locality": "string",
        "metro": "string",
        "name": "Ava Chen",
        "postalCode": "string",
        "region": "string",
        "streetAddress": "string"
      },
      "name": "Ava Chen",
      "numberFundingRounds": 1,
      "profiles": [
        [
          "string"
        ]
      ],
      "size": "string",
      "summary": "string",
      "tags": [
        [
          "string"
        ]
      ],
      "totalFundingRaised": 1,
      "twitterUrl": "https://example.com",
      "type": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliatedProfiles[]` | array<string> |  |
| `alternativeDomains[]` | array<string> |  |
| `alternativeNames[]` | array<string> |  |
| `datasetVersion` | string |  |
| `displayName` | string |  |
| `employeeCount` | number |  |
| `facebookUrl` | string |  |
| `founded` | number |  |
| `fundingStages[]` | array<string> |  |
| `headline` | string |  |
| `id` | string |  |
| `industry` | string |  |
| `industryV2` | string |  |
| `lastFundingDate` | date |  |
| `latestFundingStage` | string |  |
| `linkedinId` | string |  |
| `linkedinSlug` | string |  |
| `linkedinUrl` | string |  |
| `location.addressLine2` | string |  |
| `location.continent` | string |  |
| `location.country` | string |  |
| `location.geo` | string |  |
| `location.locality` | string |  |
| `location.metro` | string |  |
| `location.name` | string |  |
| `location.postalCode` | string |  |
| `location.region` | string |  |
| `location.streetAddress` | string |  |
| `name` | string |  |
| `numberFundingRounds` | number |  |
| `profiles[]` | array<string> |  |
| `size` | string |  |
| `summary` | string |  |
| `tags[]` | array<string> |  |
| `totalFundingRaised` | number |  |
| `twitterUrl` | string |  |
| `type` | string |  |
| `website` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /company/search` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

