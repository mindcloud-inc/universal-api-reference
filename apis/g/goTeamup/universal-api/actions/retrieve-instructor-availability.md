# GoTeamup: Retrieve Instructor Availability

Retrieves instructor availability from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-instructor-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-instructor-availability?connectionId=$CONNECTION_ID&endDate=string&id=1&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "id": "1",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-instructor-availability?${params}`, {
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
| `endDate` | string | yes | End date for the availability window. |
| `id` | number | yes | The TeamUp instructor ID. |
| `startDate` | string | yes | Start date for the availability window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "date": "string"
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
| `results[].date` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /instructors/:id/availability` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-instructor-availability.md) for the provider-specific parameters and requirements.

