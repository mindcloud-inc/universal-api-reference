# TimeRex: Get One Time URL

Retrieves a one-time URL from TimeRex.

```
GET https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-one-time-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeRex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-one-time-url?connectionId=$CONNECTION_ID&oneTimeUrlId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "oneTimeUrlId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeRex/latest/actions/get-one-time-url?${params}`, {
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
| `oneTimeUrlId` | string | yes | The TimeRex one-time URL identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TimeRex API returns.

## Native endpoint

Through the native TimeRex API, this operation is `GET /calendars/one-time-url/:oneTimeUrlId` (base URL `https://timerex.net/api/beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-one-time-url.md) for the provider-specific parameters and requirements.

