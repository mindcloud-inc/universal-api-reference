# TimeRex: Get Team

Retrieves a team by ID from TimeRex.

```
GET https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeRex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-team?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-team?${params}`, {
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
| `teamId` | string | yes | The TimeRex team identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isPrimary": true,
      "name": "Ava Chen",
      "role": "string",
      "urlPath": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isPrimary` | boolean |  |
| `name` | string |  |
| `role` | string |  |
| `urlPath` | string |  |

## Native endpoint

Through the native TimeRex API, this operation is `GET /teams/:teamId` (base URL `https://timerex.net/api/beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

