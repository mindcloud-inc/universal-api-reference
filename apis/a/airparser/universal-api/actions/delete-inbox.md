# Airparser: Delete Inbox

Deletes an existing inbox from Airparser.

```
DELETE https://connect.mindcloud.co/v1/universal/airparser/latest/actions/delete-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/delete-inbox?connectionId=$CONNECTION_ID&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airparser/latest/actions/delete-inbox?${params}`, {
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
| `inboxId` | string | yes | The Airparser inbox ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airparser API returns.

## Native endpoint

Through the native Airparser API, this operation is `DELETE /inboxes/:inbox_id` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-inbox.md) for the provider-specific parameters and requirements.

