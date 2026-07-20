# Hoversignal: List Signals



```
GET https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-signals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoversignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-signals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoversignal/latest/actions/list-signals?${params}`, {
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
      "signals": [
        {
          "id": 1,
          "isActive": true,
          "name": "Ava Chen",
          "order": 1,
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `signals` | array<object> | The list of signals in the authenticated Hoversignal site. |
| `signals[].id` | number | The signal identifier. |
| `signals[].isActive` | boolean | Whether the signal is active. |
| `signals[].name` | string | The signal name. |
| `signals[].order` | number | The display order of the signal. |
| `signals[].type` | string | The signal type. |

## Native endpoint

Through the native Hoversignal API, this operation is `GET /api/v1/signals` (base URL `https://app.hoversignal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-signals.md) for the provider-specific parameters and requirements.

