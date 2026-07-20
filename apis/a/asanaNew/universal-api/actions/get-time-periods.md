# Asana: Get time periods

Retrieves time periods from Asana.

```
GET https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-time-periods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-time-periods?connectionId=$CONNECTION_ID&workspace=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/get-time-periods?${params}`, {
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
| `endOn` | date | no |  |
| `startOn` | date | no |  |
| `workspace` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "endOn": "2026-05-07T12:00:00.000Z",
      "gid": "string",
      "period": "string",
      "resourceType": "string",
      "startOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `endOn` | date |  |
| `gid` | string |  |
| `period` | string |  |
| `resourceType` | string |  |
| `startOn` | date |  |

## Native endpoint

Through the native Asana API, this operation is `GET time_periods` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-periods.md) for the provider-specific parameters and requirements.

