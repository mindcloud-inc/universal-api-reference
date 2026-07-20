# Salesmate: Get Activity



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-activity?connectionId=$CONNECTION_ID&activityId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "activityId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/get-activity?${params}`, {
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
| `activityId` | number | yes | Salesmate activity ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isCalendarInvite": true,
      "isCompleted": true,
      "isCreatedFromSystem": true,
      "isDeleted": true,
      "lastModifiedAt": "2026-05-07T12:00:00.000Z",
      "lastModifiedBy": {},
      "lastNote": "string",
      "lastNoteAddedAt": "2026-05-07T12:00:00.000Z",
      "lastNoteAddedBy": {},
      "location": "string",
      "note": "string",
      "outcome": "string",
      "owner": {},
      "primaryCompany": {},
      "primaryContact": {},
      "purpose": "string",
      "relatedTo": {},
      "relatedToModule": "string",
      "tags": "string",
      "title": "string",
      "type": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `description` | string |  |
| `dueDate` | date |  |
| `duration` | number |  |
| `endDate` | date |  |
| `id` | number |  |
| `isCalendarInvite` | boolean |  |
| `isCompleted` | boolean |  |
| `isCreatedFromSystem` | boolean |  |
| `isDeleted` | boolean |  |
| `lastModifiedAt` | date |  |
| `lastModifiedBy` | object |  |
| `lastNote` | string |  |
| `lastNoteAddedAt` | date |  |
| `lastNoteAddedBy` | object |  |
| `location` | string |  |
| `note` | string |  |
| `outcome` | string |  |
| `owner` | object |  |
| `primaryCompany` | object |  |
| `primaryContact` | object |  |
| `purpose` | string |  |
| `relatedTo` | object |  |
| `relatedToModule` | string |  |
| `tags` | string |  |
| `title` | string |  |
| `type` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Salesmate API, this operation is `GET /activity/v4/:activityId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity.md) for the provider-specific parameters and requirements.

