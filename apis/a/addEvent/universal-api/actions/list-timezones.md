# AddEvent: List timezones



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/list-timezones
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/list-timezones?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/list-timezones?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "isDst": true,
      "localTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "tzidAbbr": "string",
      "utcOffset": 1,
      "utcOffsetHours": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isDst` | boolean |  |
| `localTime` | date |  |
| `name` | string | Timezone identifier. |
| `tzidAbbr` | string |  |
| `utcOffset` | number |  |
| `utcOffsetHours` | string |  |

## Native endpoint

Through the native AddEvent API, this operation is `GET /timezones` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timezones.md) for the provider-specific parameters and requirements.

