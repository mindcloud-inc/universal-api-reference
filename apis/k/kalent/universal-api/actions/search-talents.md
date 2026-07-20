# Kalent: Search Talents



```
GET https://connect.mindcloud.co/v1/universal/kalent/latest/actions/search-talents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kalent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kalent/latest/actions/search-talents?connectionId=$CONNECTION_ID&filters%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kalent/latest/actions/search-talents?${params}`, {
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
| `filters[]` | array<object> | yes | Required array of Kalent search filter objects. Each object follows the provider request shape and can include filterType, value, isRequired, isExcluded, isExactMatch, radius, and history. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `relatedSearchTransactionIds[]` | array<string> | no | Optional array of previous searchTransactionId values used by Kalent to continue searches without duplicate profiles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certifications": [
        {}
      ],
      "city": "string",
      "country": "string",
      "currentOrganization": {},
      "educations": [
        {}
      ],
      "experiences": [
        {}
      ],
      "firstname": "Ava",
      "gender": "string",
      "headline": "string",
      "id": "string",
      "interests": [
        "string"
      ],
      "jobTitle": "string",
      "languages": [
        {}
      ],
      "lastname": "Chen",
      "linkedinUrl": "https://example.com",
      "photoUrl": "https://example.com",
      "skills": [
        "string"
      ],
      "state": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certifications` | array<object> | Candidate certification entries. |
| `city` | string | Candidate city. |
| `country` | string | Candidate country. |
| `currentOrganization` | object | Current organization summary. |
| `educations` | array<object> | Candidate education entries. |
| `experiences` | array<object> | Candidate work experience entries. |
| `firstname` | string | Candidate first name. |
| `gender` | string | Candidate gender label. |
| `headline` | string | Candidate professional headline. |
| `id` | string | Kalent candidate identifier. |
| `interests` | array<string> | Candidate interests. |
| `jobTitle` | string | Candidate current or primary job title. |
| `languages` | array<object> | Candidate language entries. |
| `lastname` | string | Candidate last name. |
| `linkedinUrl` | string | Candidate LinkedIn profile URL. |
| `photoUrl` | string | Candidate profile photo URL. |
| `skills` | array<string> | Candidate skill labels. |
| `state` | string | Candidate state or region. |
| `summary` | string | Candidate summary or profile bio. |

## Native endpoint

Through the native Kalent API, this operation is `POST /v1/search/talents` (base URL `https://app.kalent.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-talents.md) for the provider-specific parameters and requirements.

