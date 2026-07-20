# CoachAccountable: List Appointments

Retrieves appointments from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-appointments?${params}`, {
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
| `clientId` | number | no | Filter Appointments by Client. |
| `companyId` | number | no | Filter Appointments by the Company that the Clients belong to. |
| `name` | string | no | Filter Appointments by name, supports partial matching on prefix. |
| `dateFrom` | date | no | Set to restrict Appointments returned to those starting at or after the provided value. |
| `dateTo` | date | no | Set to restrict Appointments returned to those starting at or before the provided value. |
| `includePending` | boolean | no | Set to true to include Appointments which are still just pending requests. Default: `false`. |
| `includeCanceled` | boolean | no | Set to true to include Appointments that have been canceled. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ClientID": 1,
      "CoachID": 1,
      "countsInEngagement": "string",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateCanceled": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "EngagementID": 1,
      "ID": 1,
      "location": "string",
      "name": "Ava Chen",
      "reminderSet": [
        {
          "dateSent": "2026-05-07T12:00:00.000Z",
          "dateToSend": "2026-05-07T12:00:00.000Z",
          "ID": 1,
          "isSent": true,
          "relativeMinutes": 1,
          "sendMethod": "string",
          "sendTo": "string"
        }
      ],
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ClientID` | number |  |
| `CoachID` | number |  |
| `countsInEngagement` | string |  |
| `dateAdded` | date |  |
| `dateCanceled` | date |  |
| `description` | string |  |
| `endDate` | date |  |
| `EngagementID` | number |  |
| `ID` | number |  |
| `location` | string |  |
| `name` | string |  |
| `reminderSet` | array<object> |  |
| `reminderSet[].dateSent` | date |  |
| `reminderSet[].dateToSend` | date |  |
| `reminderSet[].ID` | number |  |
| `reminderSet[].isSent` | boolean |  |
| `reminderSet[].relativeMinutes` | number |  |
| `reminderSet[].sendMethod` | string |  |
| `reminderSet[].sendTo` | string |  |
| `startDate` | date |  |
| `status` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

