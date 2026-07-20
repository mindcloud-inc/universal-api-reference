# Teamdeck: Create Time Entry

Creates a new time entry in Teamdeck.

```
POST https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": 1,
  "projectId": 1,
  "minutes": 1,
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": 1,
    "projectId": 1,
    "minutes": 1,
    "startDate": "string",
    "endDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | number | yes |  |
| `status` | number | no |  |
| `projectId` | number | yes |  |
| `minutes` | number | yes |  |
| `weekendBooking` | boolean | no |  |
| `holidaysBooking` | boolean | no |  |
| `vacationsBooking` | boolean | no |  |
| `approverId` | number | no |  |
| `description` | string | no |  |
| `externalId` | string | no |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvedAt": "string",
      "approverId": 1,
      "approverResourceId": 1,
      "creatorResourceId": 1,
      "description": "string",
      "editorResourceId": 1,
      "endDate": "string",
      "externalId": "string",
      "holidaysBooking": true,
      "id": 1,
      "minutes": 1,
      "projectId": 1,
      "requestedApproverId": 1,
      "requestedApproverResourceId": 1,
      "resourceId": 1,
      "startDate": "string",
      "status": 1,
      "vacationsBooking": true,
      "weekendBooking": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvedAt` | string |  |
| `approverId` | number |  |
| `approverResourceId` | number |  |
| `creatorResourceId` | number |  |
| `description` | string |  |
| `editorResourceId` | number |  |
| `endDate` | string |  |
| `externalId` | string |  |
| `holidaysBooking` | boolean |  |
| `id` | number |  |
| `minutes` | number |  |
| `projectId` | number |  |
| `requestedApproverId` | number |  |
| `requestedApproverResourceId` | number |  |
| `resourceId` | number |  |
| `startDate` | string |  |
| `status` | number |  |
| `vacationsBooking` | boolean |  |
| `weekendBooking` | boolean |  |

## Native endpoint

Through the native Teamdeck API, this operation is `POST /time-entries` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

