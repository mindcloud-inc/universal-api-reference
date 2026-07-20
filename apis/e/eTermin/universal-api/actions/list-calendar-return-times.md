# eTermin: List Calendar Return Times

Retrieves calendar return times from eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-return-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-return-times?connectionId=$CONNECTION_ID&calendarid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-return-times?${params}`, {
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
      "enable": true,
      "endtime": "string",
      "id": 1,
      "newday": true,
      "serviceids": "string",
      "starttime": "string",
      "weekdayidx": 1,
      "weektype": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enable` | boolean |  |
| `endtime` | string |  |
| `id` | number |  |
| `newday` | boolean |  |
| `serviceids` | string |  |
| `starttime` | string |  |
| `weekdayidx` | number |  |
| `weektype` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/calendarreturntime` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-return-times.md) for the provider-specific parameters and requirements.

