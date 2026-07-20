# Placker: Delete Webhook



```
DELETE https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&board=1235&webhook=seioqv512w0e8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board": "1235",
  "webhook": "seioqv512w0e8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placker/latest/actions/delete-webhook?${params}`, {
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
| `webhook` | string | yes | Webhook ID. Example: `seioqv512w0e8`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Placker API returns.

## Native endpoint

Through the native Placker API, this operation is `DELETE /webhook/:board/:webhook` (base URL `https://api.placker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

