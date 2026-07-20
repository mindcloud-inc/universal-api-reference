# Communi App: List Polls



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-polls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-polls?connectionId=$CONNECTION_ID&group=88729" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "88729"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-polls?${params}`, {
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
| `group` | number | yes | Default: `88729`. |
| `search` | string | no |  |
| `communiApp` | number | no | Default: `14539`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "communiApp": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "group": 1,
      "id": 1,
      "questionFormatted": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `communiApp` | number |  |
| `createdOn` | date |  |
| `group` | number |  |
| `id` | number |  |
| `questionFormatted` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/poll` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-polls.md) for the provider-specific parameters and requirements.

