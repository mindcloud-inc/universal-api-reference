# eTermin: List Service Calendars

Retrieves calendars assigned to a service in eTermin.

```
GET https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-service-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-service-calendars?connectionId=$CONNECTION_ID&serviceid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/list-service-calendars?${params}`, {
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
| `serviceid` | string | yes | ID of a service. Several service ID's can be separated with a comma (,). e.g. 45345,45346 etc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarid` | number |  |

## Native endpoint

Through the native eTermin API, this operation is `GET /api/servicecalendar` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-calendars.md) for the provider-specific parameters and requirements.

