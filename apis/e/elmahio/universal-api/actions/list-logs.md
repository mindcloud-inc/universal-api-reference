# elmah.io: List Logs

Retrieves logs from elmah.io.

```
GET https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-logs?${params}`, {
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
      "color": "string",
      "disabled": true,
      "environmentName": "Ava Chen",
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
| `color` | string |  |
| `disabled` | boolean |  |
| `environmentName` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native elmah.io API, this operation is `GET /v3/logs` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-logs.md) for the provider-specific parameters and requirements.

