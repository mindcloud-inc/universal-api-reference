# Nvoip: Delete Scheduled SMS



```
DELETE https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/delete-scheduled-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/delete-scheduled-sms?connectionId=$CONNECTION_ID&schedkey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schedkey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/delete-scheduled-sms?${params}`, {
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
| `schedkey` | string | yes | Identifier of the scheduled SMS to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nvoip API returns.

## Native endpoint

Through the native Nvoip API, this operation is `DELETE /delete/sched/torpedo` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-scheduled-sms.md) for the provider-specific parameters and requirements.

