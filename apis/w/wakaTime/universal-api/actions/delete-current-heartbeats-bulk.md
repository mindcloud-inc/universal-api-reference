# WakaTime: Delete Current Heartbeats Bulk

Deletes multiple heartbeats from WakaTime.

```
DELETE https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/delete-current-heartbeats-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WakaTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/delete-current-heartbeats-bulk?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wakaTime/latest/actions/delete-current-heartbeats-bulk?${params}`, {
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
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |

## Native endpoint

Through the native WakaTime API, this operation is `DELETE /users/current/heartbeats.bulk` (base URL `https://api.wakatime.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-current-heartbeats-bulk.md) for the provider-specific parameters and requirements.

