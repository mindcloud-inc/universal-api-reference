# KYVE: Get Team Vesting Status By Time



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-team-vesting-status-by-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-team-vesting-status-by-time?connectionId=$CONNECTION_ID&id=string&time=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "time": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-team-vesting-status-by-time?${params}`, {
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
| `id` | string | yes | Team vesting account ID. |
| `time` | string | yes | Unix timestamp to calculate vesting progress at. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "plan": {},
      "request_date": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plan` | object |  |
| `request_date` | string |  |
| `status` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/team/v1beta1/team_vesting_status_by_time/{id}/{time}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-vesting-status-by-time.md) for the provider-specific parameters and requirements.

