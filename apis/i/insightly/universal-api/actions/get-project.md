# Insightly: Get Project

Retrieves a project from Insightly by ID.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/get-project?${params}`, {
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
| `projectId` | number | yes | The Project ID. |

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

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Projects/:projectId` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

