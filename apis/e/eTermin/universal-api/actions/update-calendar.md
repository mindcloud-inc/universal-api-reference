# eTermin: Update Calendar

Updates an existing calendar in eTermin.

```
PUT https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-calendar', {
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
| `id` | number | yes | ID of the calendar |
| `calendarname` | string | no | Name of the calendar. This name is used for all languages |
| `descriptionlanguagecode` | string | no | e.g. descriptionde adds additional information for this calendar in German language. descriptionen in English etc. |
| `descriptiondisplaytype` | number | no | defines if the description is shown on the bookingpage <br> 0 = not shown<br> 1 = shown under calendar name<br> 2 = shown as tooltip |
| `enablecapacity` | boolean | no | Several appointments can be booked at the same time |
| `maxcapacity` | number | no | Maximum capacity of appointments that can be booked at the same time |
| `differentlocation` | boolean | no | The location of the calendar is different than the main location |
| `name` | string | no | Name of the different company name |
| `street` | string | no | Street |
| `zip` | string | no | ZIP |
| `city` | string | no | City |
| `country` | string | no | Country |
| `telephone` | string | no | Telephone |
| `mobilephone` | string | no | MobilePhone |
| `emaillocation` | string | no | Email |
| `web` | string | no | Internet address |
| `completeappointmentwithinopeninghours` | boolean | no | If you have configured services where free, idle or down times between appointments occur, you can define whether these should be within the defined available times. |
| `smsnotification` | boolean | no | Employee will be informed by SMS if an appointment was booked |
| `smsphonenumber` | string | no | Number of the phone |
| `smstimespanhours` | number | no | Threshold (in hours) if SMS should be sent |
| `calendartype` | boolean | no | Main calendar (0) or sub calendar (1) |
| `limittoduration` | number | no | Calendar can only handle appointments that have a certain length (defined in maxduration) |
| `maxduration` | number | no | Maximum appointment duration (minutes) |
| `waitingnr` | boolean | no | Calculate waiting number |
| `wnprefix` | string | no | Prefix of the waiting number |
| `wnstartnr` | number | no | Start number of the waiting number |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eTermin API returns.

## Native endpoint

Through the native eTermin API, this operation is `PUT /api/calendar` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar.md) for the provider-specific parameters and requirements.

