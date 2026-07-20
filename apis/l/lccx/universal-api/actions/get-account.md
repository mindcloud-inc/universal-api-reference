# lc.cx: Get Account

Retrieves account details from lc.cx.

```
GET https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-account?${params}`, {
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
      "max_shortlinks": 1,
      "plan": "string",
      "reset_date": "2026-05-07T12:00:00.000Z",
      "shortlinks_usage": 1,
      "tags": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `max_shortlinks` | number |  |
| `plan` | string |  |
| `reset_date` | date |  |
| `shortlinks_usage` | number |  |
| `tags` | boolean |  |
| `username` | string |  |

## Native endpoint

Through the native lc.cx API, this operation is `GET /account` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

