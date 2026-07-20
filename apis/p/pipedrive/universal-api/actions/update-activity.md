# Pipedrive: Update Activity

Updates an existing activity in Pipedrive.

```
PUT https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dueDate` | string | no | Due date (YYYY-MM-DD). |
| `dueTime` | string | no | Due time (HH:mm). |
| `duration` | string | no | Duration in HH:mm format. |
| `id` | number | yes | Unique ID of the activity to update. |
| `leadId` | string | no | Linked lead ID. |
| `note` | string | no | Activity note. |
| `priority` | string | no | Activity priority. |
| `subject` | string | no | Activity subject. |
| `type` | string | no | Activity type. |
| `ownerId` | number | no | Owner user ID. |
| `dealId` | number | no | Linked deal ID. |
| `personId` | number | no | Linked person ID. |
| `orgId` | number | no | Linked organization ID. |
| `done` | boolean | no | Completion state. |

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

Through the native Pipedrive API, this operation is `PATCH v2/activities/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

