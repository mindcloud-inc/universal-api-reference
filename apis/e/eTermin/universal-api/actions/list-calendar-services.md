# eTermin: List Calendar Services

Retrieves services assigned to a calendar in eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-calendar-services?${params}`, {
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
| `calendarid` | string | no | ID of the calendar you want the service assignments |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarid": 1,
      "id": 1,
      "serviceid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarid` | number |  |
| `id` | number |  |
| `serviceid` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/calendarservice` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-services.md) for the provider-specific parameters and requirements.

