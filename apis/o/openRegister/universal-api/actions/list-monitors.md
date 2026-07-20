# OpenRegister: List Monitors

Retrieves existing monitor records from OpenRegister.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/list-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/list-monitors?${params}`, {
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
      "items": [
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
| `items` | array<object> | Configured monitors. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v1/monitor` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitors.md) for the provider-specific parameters and requirements.

