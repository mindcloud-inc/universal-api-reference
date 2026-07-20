# Teamdeck: List Time Entries

Retrieves time entries from your Teamdeck organization.

```
GET https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamdeck `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamdeck/latest/actions/list-time-entries?${params}`, {
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
| `fields` | string | no |  |
| `expand` | string | no |  |
| `resourceIds` | string | no |  |
| `projectIds` | string | no |  |
| `externalIds` | string | no |  |
| `startDateFrom` | string | no |  |
| `startDateTo` | string | no |  |
| `endDateFrom` | string | no |  |
| `endDateTo` | string | no |  |
| `date` | string | no |  |

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

Through the native Teamdeck API, this operation is `GET /time-entries` (base URL `https://api.teamdeck.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

