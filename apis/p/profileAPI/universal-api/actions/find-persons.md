# profileAPI: Find Persons

Finds persons in profileAPI by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/find-persons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a profileAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/find-persons?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/profileAPI/latest/actions/find-persons?${params}`, {
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
| `filters` | object | yes | Filter groups containing all/any filter arrays. Example: `[object Object]`. |
| `limit` | number | no | Maximum number of persons to return. Official docs list default 10 and maximum 100. Default: `10`. Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthYear": 1,
      "countryCode": "string",
      "educations": [
        {
          "degree": "string",
          "institutionDivision": "string",
          "institutionDivisionDepartment": "string",
          "institutionName": "Ava Chen",
          "major": "string"
        }
      ],
      "experiences": [
        {
          "endedAt": "2026-05-07T12:00:00.000Z",
          "isCurrent": true,
          "name": "Ava Chen",
          "startedAt": "2026-05-07T12:00:00.000Z",
          "title": "string"
        }
      ],
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "linkedInUrl": "https://example.com",
      "name": "Ava Chen",
      "photoUrl": "https://example.com",
      "skillTags": [
        "string"
      ],
      "unitedStatesCity": "string",
      "unitedStatesRegion": "string",
      "unitedStatesStateCode": "string",
      "worldRegion": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthYear` | number |  |
| `countryCode` | string |  |
| `educations[].degree` | string |  |
| `educations[].institutionDivision` | string |  |
| `educations[].institutionDivisionDepartment` | string |  |
| `educations[].institutionName` | string |  |
| `educations[].major` | string |  |
| `experiences[].endedAt` | date |  |
| `experiences[].isCurrent` | boolean |  |
| `experiences[].name` | string |  |
| `experiences[].startedAt` | date |  |
| `experiences[].title` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `linkedInUrl` | string |  |
| `name` | string |  |
| `photoUrl` | string |  |
| `skillTags[]` | string |  |
| `unitedStatesCity` | string |  |
| `unitedStatesRegion` | string |  |
| `unitedStatesStateCode` | string |  |
| `worldRegion` | string |  |

## Native endpoint

Through the native profileAPI API, this operation is `POST /persons/find` (base URL `https://api.profileapi.com/2024-03-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-persons.md) for the provider-specific parameters and requirements.

