# Pipedrive: Get Activities

Retrieves activities from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-activities?${params}`, {
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
| `cursor` | string | no | Pagination cursor. |
| `filterId` | number | no | Saved filter ID for activities. |
| `ids` | string | no | Comma-separated activity IDs. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `leadId` | string | no | Filter by lead ID. |
| `sortBy` | string | no | Sort field. |
| `sortDirection` | string | no | Sort direction, asc or desc. |
| `updatedSince` | string | no | Return activities updated after this datetime. |
| `updatedUntil` | string | no | Return activities updated before this datetime. |
| `ownerId` | number | no | Owner user ID. |
| `dealId` | number | no | Filter by deal ID. |
| `personId` | number | no | Filter by person ID. |
| `orgId` | number | no | Filter by organization ID. |
| `done` | boolean | no | Filter by completion state. |
| `limit` | number | no | Max results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "busy": true,
      "conferenceMeetingClient": {},
      "conferenceMeetingId": {},
      "conferenceMeetingUrl": {},
      "creatorUserId": 1,
      "dealId": {},
      "done": true,
      "dueDate": "string",
      "dueTime": {},
      "duration": {},
      "id": 1,
      "isDeleted": true,
      "leadId": {},
      "location": {},
      "markedAsDoneTime": {},
      "note": {},
      "orgId": {},
      "ownerId": 1,
      "personId": {},
      "priority": {},
      "projectId": {},
      "publicDescription": {},
      "subject": "string",
      "type": "string",
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `busy` | boolean |  |
| `conferenceMeetingClient` | object |  |
| `conferenceMeetingId` | object |  |
| `conferenceMeetingUrl` | object |  |
| `creatorUserId` | number |  |
| `dealId` | object |  |
| `done` | boolean |  |
| `dueDate` | string |  |
| `dueTime` | object |  |
| `duration` | object |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `leadId` | object |  |
| `location` | object |  |
| `markedAsDoneTime` | object |  |
| `note` | object |  |
| `orgId` | object |  |
| `ownerId` | number |  |
| `personId` | object |  |
| `priority` | object |  |
| `projectId` | object |  |
| `publicDescription` | object |  |
| `subject` | string |  |
| `type` | string |  |
| `updateTime` | string |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/activities` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-activities.md) for the provider-specific parameters and requirements.

