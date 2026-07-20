# Placker: Get Webhook Example Data



```
GET https://connect.mindcloud.co/v1/universal/placker/latest/actions/get-webhook-example-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placker/latest/actions/get-webhook-example-data?connectionId=$CONNECTION_ID&board=1235&events%5B%5D=card_created" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board": "1235",
  "events[]": "card_created"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/get-webhook-example-data?${params}`, {
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
| `board` | number | yes | Board ID. Example: `1235`. |
| `events[]` | array<string> | yes | Event types to get example data for. Example: `card_created`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `GET /webhook/:board/example` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-example-data.md) for the provider-specific parameters and requirements.

