# Jaicob: Retrieve Vacancy



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-vacancy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-vacancy?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-vacancy?${params}`, {
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
| `id` | string | yes | Vacancy identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationSettings": {},
      "bannerImage": "string",
      "client": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "educationLevel": {},
      "employmentType": "string",
      "id": "string",
      "industry": {},
      "jobCategory": {},
      "languages": [
        {}
      ],
      "location": {},
      "locations": [
        {}
      ],
      "salary": {},
      "seniority": {},
      "skills": [
        {}
      ],
      "startDate": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workingHours": {},
      "yearsOfExperience": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationSettings` | object |  |
| `bannerImage` | string |  |
| `client` | object |  |
| `createdAt` | date |  |
| `description` | string |  |
| `educationLevel` | object |  |
| `employmentType` | string |  |
| `id` | string |  |
| `industry` | object |  |
| `jobCategory` | object |  |
| `languages` | array<object> |  |
| `location` | object |  |
| `locations` | array<object> |  |
| `salary` | object |  |
| `seniority` | object |  |
| `skills` | array<object> |  |
| `startDate` | date |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `workingHours` | object |  |
| `yearsOfExperience` | number |  |

## Native endpoint

Through the native Jaicob API, this operation is `GET /vacancies/public/[:id]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-vacancy.md) for the provider-specific parameters and requirements.

