# Sendible: List Calendar Messages



```
GET https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-calendar-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-calendar-messages?connectionId=$CONNECTION_ID&from=string&to=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "string",
  "to": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendible/latest/actions/list-calendar-messages?${params}`, {
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
| `from` | string | yes | Start datetime in YYYY-MM-DD HH:mm:ss format. |
| `pageSize` | number | no | Requested page size. |
| `perPage` | number | no | Requested page size alias. |
| `to` | string | yes | End datetime in YYYY-MM-DD HH:mm:ss format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paging": {},
      "result": [
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
| `paging` | object |  |
| `result` | array<object> |  |

## Native endpoint

Through the native Sendible API, this operation is `GET 0.1/tw/messages` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-messages.md) for the provider-specific parameters and requirements.

