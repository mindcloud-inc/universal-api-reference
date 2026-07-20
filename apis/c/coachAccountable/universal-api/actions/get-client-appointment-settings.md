# CoachAccountable: Get Client Appointment Settings

Retrieves client appointment settings from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-appointment-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-appointment-settings?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/get-client-appointment-settings?${params}`, {
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
| `clientId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointmentTypes": "string",
      "attachICSFiles": true,
      "isAllGenerallyAvailable": true,
      "selfSchedulingEmailConfirmations": true,
      "selfSchedulingRule": "string",
      "specificSet": [
        {
          "CoachID": 1,
          "coachName": "Ava Chen",
          "ID": 1,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointmentTypes` | string |  |
| `attachICSFiles` | boolean |  |
| `isAllGenerallyAvailable` | boolean |  |
| `selfSchedulingEmailConfirmations` | boolean |  |
| `selfSchedulingRule` | string |  |
| `specificSet` | array<object> |  |
| `specificSet[].CoachID` | number |  |
| `specificSet[].coachName` | string |  |
| `specificSet[].ID` | number |  |
| `specificSet[].name` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client-appointment-settings.md) for the provider-specific parameters and requirements.

