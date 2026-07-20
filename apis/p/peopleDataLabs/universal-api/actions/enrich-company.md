# People Data Labs: Enrich Company



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-company?connectionId=$CONNECTION_ID&profile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-company?${params}`, {
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
| `profile` | string | yes | LinkedIn company profile URL used for deterministic company enrichment. |

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
      "likelihood": 1,
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
      "status": 1,
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
| `likelihood` | number |  |
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
| `status` | number |  |
| `summary` | string |  |
| `tags[]` | array<string> |  |
| `totalFundingRaised` | number |  |
| `twitterUrl` | string |  |
| `type` | string |  |
| `website` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /company/enrich` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company.md) for the provider-specific parameters and requirements.

