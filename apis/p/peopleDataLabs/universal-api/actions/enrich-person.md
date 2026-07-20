# People Data Labs: Enrich Person



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-person?connectionId=$CONNECTION_ID&profile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/enrich-person?${params}`, {
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
| `profile` | string | yes | A social profile that the person has used. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countries": [
        [
          "string"
        ]
      ],
      "datasetVersion": "string",
      "education": [
        [
          {}
        ]
      ],
      "experience": [
        [
          {}
        ]
      ],
      "facebookUrl": "https://example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "industry": "string",
      "interests": [
        [
          "string"
        ]
      ],
      "jobCompanyId": "string",
      "jobCompanyIndustryV2": "string",
      "jobCompanyLinkedinId": "https://example.com",
      "jobCompanyLinkedinUrl": "https://example.com",
      "jobCompanyName": "Ava Chen",
      "jobCompanySize": "string",
      "jobCompanyWebsite": "string",
      "jobLastChanged": "2026-05-07T12:00:00.000Z",
      "jobLastVerified": "2026-05-07T12:00:00.000Z",
      "jobStartDate": "string",
      "jobTitle": "string",
      "jobTitleClass": "string",
      "jobTitleLevels": [
        [
          "string"
        ]
      ],
      "jobTitleRole": "string",
      "jobTitleSubRole": "string",
      "lastName": "Chen",
      "linkedinId": "https://example.com",
      "linkedinUrl": "https://example.com",
      "linkedinUsername": "https://example.com",
      "locationContinent": "string",
      "locationCountry": "string",
      "profiles": [
        [
          {}
        ]
      ],
      "skills": [
        [
          "string"
        ]
      ],
      "twitterUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries[]` | array<string> |  |
| `datasetVersion` | string |  |
| `education[]` | array<object> |  |
| `experience[]` | array<object> |  |
| `facebookUrl` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `industry` | string |  |
| `interests[]` | array<string> |  |
| `jobCompanyId` | string |  |
| `jobCompanyIndustryV2` | string |  |
| `jobCompanyLinkedinId` | string |  |
| `jobCompanyLinkedinUrl` | string |  |
| `jobCompanyName` | string |  |
| `jobCompanySize` | string |  |
| `jobCompanyWebsite` | string |  |
| `jobLastChanged` | date |  |
| `jobLastVerified` | date |  |
| `jobStartDate` | string |  |
| `jobTitle` | string |  |
| `jobTitleClass` | string |  |
| `jobTitleLevels[]` | array<string> |  |
| `jobTitleRole` | string |  |
| `jobTitleSubRole` | string |  |
| `lastName` | string |  |
| `linkedinId` | string |  |
| `linkedinUrl` | string |  |
| `linkedinUsername` | string |  |
| `locationContinent` | string |  |
| `locationCountry` | string |  |
| `profiles[]` | array<object> |  |
| `skills[]` | array<string> |  |
| `twitterUrl` | string |  |

## Native endpoint

Through the native People Data Labs API, this operation is `GET /person/enrich` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-person.md) for the provider-specific parameters and requirements.

