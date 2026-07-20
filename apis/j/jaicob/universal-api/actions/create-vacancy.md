# Jaicob: Create Vacancy



```
POST https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-vacancy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-vacancy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "description": "string",
  "yearsOfExperience": 1,
  "workingHours": {},
  "salary": {},
  "location": {},
  "educationLevelId": 1,
  "seniorityId": 1,
  "industryId": 1,
  "jobCategoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/create-vacancy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "description": "string",
    "yearsOfExperience": 1,
    "workingHours": {},
    "salary": {},
    "location": {},
    "educationLevelId": 1,
    "seniorityId": 1,
    "industryId": 1,
    "jobCategoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `description` | string | yes |  |
| `yearsOfExperience` | number | yes |  |
| `employmentType` | string | no |  |
| `workingHours` | object | yes |  |
| `salary` | object | yes |  |
| `location` | object | yes |  |
| `tags[]` | array<string> | no |  |
| `locationIds[]` | array<string> | no |  |
| `educationLevelId` | number | yes |  |
| `seniorityId` | number | yes |  |
| `industryId` | number | yes |  |
| `jobCategoryId` | number | yes |  |
| `bannerImage` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Jaicob API, this operation is `POST /vacancies` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vacancy.md) for the provider-specific parameters and requirements.

