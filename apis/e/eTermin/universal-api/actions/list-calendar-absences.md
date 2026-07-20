# eTermin: List Calendar Absences

Retrieves calendar absences from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-absences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-absences?connectionId=$CONNECTION_ID&calendarid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-absences?${params}`, {
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
| `calendarid` | number | yes | ID of the calendar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dynamicdays": 1,
      "enddate": "string",
      "id": 1,
      "nwtype": 1,
      "reason": "string",
      "startdate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dynamicdays` | number |  |
| `enddate` | string |  |
| `id` | number |  |
| `nwtype` | number |  |
| `reason` | string |  |
| `startdate` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/calendarsnonworkingtimes` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-absences.md) for the provider-specific parameters and requirements.

