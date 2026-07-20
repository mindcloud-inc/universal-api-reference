# lc.cx: Get Link Click Statistics

Retrieves click statistics for a short link in lc.cx.

```
GET https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-link-click-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lc.cx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-link-click-statistics?connectionId=$CONNECTION_ID&linkId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lccx/latest/actions/get-link-click-statistics?${params}`, {
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
| `linkId` | string | yes | The ID of the link whose click statistics you want. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native lc.cx API returns.

## Native endpoint

Through the native lc.cx API, this operation is `GET /statistics/links/:id/clicks` (base URL `https://api.lc.cx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-click-statistics.md) for the provider-specific parameters and requirements.

