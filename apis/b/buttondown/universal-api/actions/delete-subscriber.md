# Buttondown: Delete Subscriber

Deletes an existing subscriber from Buttondown.

```
DELETE https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/delete-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/delete-subscriber?connectionId=$CONNECTION_ID&id_or_email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id_or_email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/delete-subscriber?${params}`, {
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
| `id_or_email` | string | yes | Subscriber ID or email address. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Buttondown API returns.

## Native endpoint

Through the native Buttondown API, this operation is `DELETE /subscribers/:id_or_email` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber.md) for the provider-specific parameters and requirements.

