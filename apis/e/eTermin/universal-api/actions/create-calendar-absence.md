# eTermin: Create Calendar Absence

Creates a new calendar absence in eTermin.

```
POST https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-calendar-absence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-calendar-absence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appcalendarid": 1,
  "startdate": "string",
  "enddate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-calendar-absence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appcalendarid": 1,
    "startdate": "string",
    "enddate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appcalendarid` | number | yes | ID of the calendar. Use the "Calendar - Get calendar details" function to get a list with all available calendars. |
| `startdate` | string | yes | Start time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `enddate` | string | yes | End time of the absence. Format: yyyy-mm-dd HH:MM e.g. 2017-10-24 18:00 |
| `reason` | string | no | Reason or note for the absence. |
| `nwtype` | boolean | no | Indicates if the absence is dynamic. |
| `dynamicdays` | number | no | Number of days for the dynamic absence to begin (nwtype has to be 1). |
| `dynamicdaysduration` | number | no | Number of days for the dynamic absence to last (nwtype has to be 1). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eTermin API returns.

## Native endpoint

Through the native eTermin API, this operation is `POST /api/calendarsnonworkingtimes` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar-absence.md) for the provider-specific parameters and requirements.

