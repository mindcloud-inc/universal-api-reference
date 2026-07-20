# eTermin: Update Calendar Absence

Updates an existing calendar absence in eTermin.

```
PUT https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-calendar-absence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-calendar-absence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-calendar-absence', {
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
| `id` | number | yes | ID of the absence. |
| `appcalendarid` | number | no | ID of the calendar. Use the "Calendar - Get calendar details" function to get a list with all available calendars. |
| `startdate` | string | no | Start time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `enddate` | string | no | End time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `reason` | string | no | Reason or note for the absence. |
| `nwtype` | boolean | no | Indicates if the absence is dynamic. |
| `dynamicdays` | number | no | Number of days for the dynamic absence (nwtype has to be 1). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eTermin API returns.

## Native endpoint

Through the native eTermin API, this operation is `PUT /api/calendarsnonworkingtimes` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-calendar-absence.md) for the provider-specific parameters and requirements.

