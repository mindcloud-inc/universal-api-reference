# White Swan: List Earnings Events

Retrieves earnings events from White Swan.

```
GET https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-earnings-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-earnings-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-earnings-events?${params}`, {
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
| `clientEmail` | string | no | Optionally filter earnings events by client email. |
| `userEmail` | string | no | Optionally filter earnings events by account user email. |
| `lookback` | number | no | Optionally limit events to the last N days. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native White Swan API returns.

## Native endpoint

Through the native White Swan API, this operation is `POST /earnings_event` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-earnings-events.md) for the provider-specific parameters and requirements.

