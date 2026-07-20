# TalentHR: List Published Job Positions

Retrieves published job positions from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-published-job-positions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-published-job-positions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-published-job-positions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "appliedCount": 1,
      "availableSteps": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "departmentName": "Ava Chen",
      "employmentStatusId": 1,
      "employmentStatusName": "Ava Chen",
      "endDate": "2026-05-07T12:00:00.000Z",
      "hasApplications": true,
      "hiredCount": 1,
      "id": 1,
      "isRemote": true,
      "jobDescription": "string",
      "jobPositionStatusId": 1,
      "jobPositionStatusName": "Ava Chen",
      "jobPositionStatusSlug": "string",
      "jobPositionTitle": "string",
      "locationAddress": "string",
      "locationId": 1,
      "locationName": "Ava Chen",
      "processedCount": 1,
      "publishDate": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appliedCount` | number |  |
| `availableSteps` | array<object> |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `departmentId` | number |  |
| `departmentName` | string |  |
| `employmentStatusId` | number |  |
| `employmentStatusName` | string |  |
| `endDate` | date |  |
| `hasApplications` | boolean |  |
| `hiredCount` | number |  |
| `id` | number |  |
| `isRemote` | boolean |  |
| `jobDescription` | string |  |
| `jobPositionStatusId` | number |  |
| `jobPositionStatusName` | string |  |
| `jobPositionStatusSlug` | string |  |
| `jobPositionTitle` | string |  |
| `locationAddress` | string |  |
| `locationId` | number |  |
| `locationName` | string |  |
| `processedCount` | number |  |
| `publishDate` | date |  |
| `slug` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /job-positions/published` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-published-job-positions.md) for the provider-specific parameters and requirements.

