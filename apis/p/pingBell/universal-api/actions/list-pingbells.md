# PingBell: List PingBells

Retrieves PingBells from your PingBell account.

```
GET https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/list-pingbells
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PingBell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/list-pingbells?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingBell/latest/actions/list-pingbells?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The PingBell ID. |
| `name` | string | The PingBell name. |

## Native endpoint

Through the native PingBell API, this operation is `GET /userPingbells` (base URL `https://app.pingbell.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pingbells.md) for the provider-specific parameters and requirements.

