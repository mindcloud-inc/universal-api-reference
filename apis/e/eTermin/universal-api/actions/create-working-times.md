# eTermin: Create Working Times

Creates new working times in eTermin.

```
POST https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-working-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-working-times" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "start": "string",
  "end": "string",
  "calendarid": 1,
  "weekday": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-working-times', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "start": "string",
    "end": "string",
    "calendarid": 1,
    "weekday": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | yes | Start time of the slot, e.g. 09:00 |
| `end` | string | yes | End time of the slot, e.g. 17:00 |
| `calendarid` | number | yes | ID of the calendar |
| `weekday` | string | yes | ID of the weekday 1 = Sunday, 7 = Saturday. You can add several weekdays separated by a comma e.g. 2,3,5 |
| `enable` | number | no | 0 if the time slot should exist but not being considered yet |
| `slottype` | number | no | 0 if time slots should be valid for internal and external (online booked) appointments. 1 if timeslots are only valid for interal (manually entered) appointments |
| `validwithserviceid` | string | no | List of services that work with this working slot |
| `allserviceidsrequired` | number | no | Defines how the validity of the services are checked. Exclusive means that only the services provided with the parameter validwithserviceid are allowed. If not exclusive, every service the calendar is activated for can be used. <br> 0 = one service needs to be selected <br> 1 = all services need to be selected exclusively <br> 2 = all services need to be selected <br> 3 = one service needs to be selected exclusively) |
| `nrapps` | number | no | Amount of appointments that are bookable in this working slot. (-1 = unlimited) |
| `weektype` | number | no | Defines in which interval the time slot should be shown <br> 0 = Every week <br> 1 = Odd weeks <br> 2 = Even weeks <br> 3 = First occurrence in month <br> 4 = second occurrence in month <br> 5 = third occurrence in month <br> 6 = fourth occurrence in month <br> 7 = Every 3 weeks first occurrence <br> 8 = Every 3 weeks second occurrence <br> 9 = Every 3 weeks third occurrence <br> 10 = fifth occurrence in month <br> 11 = Every 4 weeks first occurrence <br> 12 = Every 4 weeks second occurrence <br> 13 = Every 4 weeks third occurrence <br> 14 = Every 4 weeks fourth occurrence |
| `locationid` | number | no | ID of the location for this working slot if locations are used in working times |
| `calendarintervalid` | number | no | ID of the period for this working slot if periods are used in working times |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": 1,
      "statusmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | number |  |
| `statusmsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `POST /api/workingtimes` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-working-times.md) for the provider-specific parameters and requirements.

