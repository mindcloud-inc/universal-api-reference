# People Data Labs: Search People



```
GET https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a People Data Labs `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/search-people?connectionId=$CONNECTION_ID&limit=25&offset=0&sql=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "sql": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peopleDataLabs/latest/actions/search-people?${params}`, {
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
| `sql` | string | yes | SQL query used to search People Data Labs person records. Must be of the form SELECT * FROM person WHERE ... |

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
      "githubUrl": "https://example.com",
      "id": "string",
      "industry": "string",
      "interests": [
        [
          "string"
        ]
      ],
      "jobCompanyId": "string",
      "jobCompanyIndustry": "string",
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
| `githubUrl` | string |  |
| `id` | string |  |
| `industry` | string |  |
| `interests[]` | array<string> |  |
| `jobCompanyId` | string |  |
| `jobCompanyIndustry` | string |  |
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

Through the native People Data Labs API, this operation is `GET /person/search` (base URL `https://api.peopledatalabs.com/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

