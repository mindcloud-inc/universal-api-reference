# actiTIME: Get User Schedule

Retrieves a user's schedule from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-user-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-user-schedule?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-user-schedule?${params}`, {
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
| `dateFrom` | string | no | Start date of requested schedule in YYYY-MM-DD format. |
| `dateTo` | string | no | End date of requested schedule in YYYY-MM-DD format. |
| `uid` | string | yes | User ID or username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateFrom": "2026-05-07T12:00:00.000Z",
      "dateTo": "2026-05-07T12:00:00.000Z",
      "schedule": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateFrom` | date | Start date of the returned schedule. |
| `dateTo` | date | End date of the returned schedule. |
| `schedule[]` | number | Daily work duration in minutes. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /users/:uid/schedule` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-schedule.md) for the provider-specific parameters and requirements.

