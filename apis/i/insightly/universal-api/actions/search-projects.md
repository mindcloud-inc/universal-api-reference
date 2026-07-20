# Insightly: Search Projects

Finds projects in Insightly by search filters.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-projects?${params}`, {
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
| `fieldName` | string | no | Filter projects by this field name. |
| `fieldValue` | string | no | Filter projects by this field value. |
| `updatedAfterUtc` | string | no | Return projects updated after this UTC timestamp. |
| `brief` | boolean | no | Return only top-level properties for each project. |
| `countTotal` | boolean | no | Return the total-record count in the response headers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDate": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "opportunityId": 1,
      "ownerUserId": 1,
      "pipelineId": 1,
      "projectDetails": "string",
      "projectId": 1,
      "projectName": "Ava Chen",
      "responsibleUserId": 1,
      "stageId": 1,
      "startedDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDate` | date |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `imageUrl` | string |  |
| `lastActivityDateUtc` | date |  |
| `nextActivityDateUtc` | date |  |
| `opportunityId` | number |  |
| `ownerUserId` | number |  |
| `pipelineId` | number |  |
| `projectDetails` | string |  |
| `projectId` | number |  |
| `projectName` | string |  |
| `responsibleUserId` | number |  |
| `stageId` | number |  |
| `startedDate` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Projects/Search` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-projects.md) for the provider-specific parameters and requirements.

