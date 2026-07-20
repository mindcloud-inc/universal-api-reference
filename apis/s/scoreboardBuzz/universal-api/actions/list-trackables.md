# Scoreboard Buzz: List Trackables

Retrieves trackables from Scoreboard Buzz.

```
GET https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-trackables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoreboard Buzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-trackables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-trackables?${params}`, {
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
      "id": 1,
      "trackable_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Scoreboard Buzz trackable ID. |
| `trackable_name` | string | Trackable display name. |

## Native endpoint

Through the native Scoreboard Buzz API, this operation is `GET /trackables` (base URL `https://api.scoreboardbuzz.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trackables.md) for the provider-specific parameters and requirements.

