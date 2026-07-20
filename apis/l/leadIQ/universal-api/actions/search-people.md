# LeadIQ: Search People



```
GET https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LeadIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/search-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIQ/latest/actions/search-people?${params}`, {
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
| `id` | string | no | Search by the LeadIQ person identifier. |
| `firstName` | string | no | Search by first name. |
| `lastName` | string | no | Search by last name. |
| `fullName` | string | no | Search by a person's full name. |
| `email` | string | no | Search by email address. |
| `phone` | string | no | Search by phone number. |
| `linkedinId` | string | no | Search by the LinkedIn member ID. |
| `linkedinUrl` | string | no | Search by the LinkedIn profile URL. |
| `company` | object | no | Optional CompanyDetails object. Supported keys: companyId, name, domain, emailDomain, linkedinId, country, searchInPastCompanies, strict. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `middleName` | string | no | Search by middle name. |
| `hashedEmail` | string | no | Search by a SHA256 hashed email address. |
| `workEmailStatusIn[]` | array<string> | no | Optional array of email verification statuses: Verified, Unverified, VerifiedLikely, Invalid. |
| `containsWorkContactInfo` | boolean | no | When true, only return people with work contact info. |
| `profileFilter[]` | array<string> | no | Optional array of profile filters: HasVerifiedWorkPhone, HasPersonalPhone, HasWorkPhone, HasPersonalEmail, HasVerifiedWorkEmail, HasWorkEmail. |
| `includeInvalid` | boolean | no | When true, include Invalid emails in the result. |
| `qualityFilter` | object | no | Optional QualityFilter object. Currently supports the phone enum quality filter. |
| `minConfidence` | number | no | Minimum person confidence score from 0 to 100. |
| `limit` | number | no | Maximum number of people to return. |
| `skip` | number | no | Number of matching people to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": 1,
      "currentPositions": [
        {
          "companyInfo": {
            "domain": "string",
            "id": "string",
            "industry": "string",
            "linkedinId": "https://example.com",
            "linkedinUrl": "https://example.com",
            "name": "Ava Chen",
            "numberOfEmployees": 1
          },
          "function": "string",
          "matchedQuery": true,
          "seniority": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "id": "string",
      "linkedin": {
        "linkedinId": "https://example.com",
        "linkedinUrl": "https://example.com",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "location": {
        "areaLevel1": "string",
        "city": "string",
        "country": "string",
        "countryCode2": "string",
        "fullAddress": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "name": {
        "first": "Ava Chen",
        "fullName": "Ava Chen",
        "last": "Ava Chen",
        "middle": "Ava Chen"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | number |  |
| `currentPositions[].companyInfo.domain` | string |  |
| `currentPositions[].companyInfo.id` | string |  |
| `currentPositions[].companyInfo.industry` | string |  |
| `currentPositions[].companyInfo.linkedinId` | string |  |
| `currentPositions[].companyInfo.linkedinUrl` | string |  |
| `currentPositions[].companyInfo.name` | string |  |
| `currentPositions[].companyInfo.numberOfEmployees` | number |  |
| `currentPositions[].function` | string |  |
| `currentPositions[].matchedQuery` | boolean |  |
| `currentPositions[].seniority` | string |  |
| `currentPositions[].title` | string |  |
| `currentPositions[].updatedAt` | date |  |
| `id` | string |  |
| `linkedin.linkedinId` | string |  |
| `linkedin.linkedinUrl` | string |  |
| `linkedin.updatedAt` | date |  |
| `location.areaLevel1` | string |  |
| `location.city` | string |  |
| `location.country` | string |  |
| `location.countryCode2` | string |  |
| `location.fullAddress` | string |  |
| `location.updatedAt` | date |  |
| `name.first` | string |  |
| `name.fullName` | string |  |
| `name.last` | string |  |
| `name.middle` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native LeadIQ API, this operation is `POST graphql` (base URL `https://api.leadiq.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

