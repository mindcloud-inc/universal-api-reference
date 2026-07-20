# AvoSMS: Delete Sender

Deletes an existing sender from AvoSMS.

```
DELETE https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AvoSMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-sender?connectionId=$CONNECTION_ID&sender=MCLD31A" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sender": "MCLD31A"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoSMS/latest/actions/delete-sender?${params}`, {
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
| `sender` | string | yes | Sender name between 3 and 11 characters Example: `MCLD31A`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AvoSMS API returns.

## Native endpoint

Through the native AvoSMS API, this operation is `POST /v1/sender/delete` (base URL `https://api.avosms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sender.md) for the provider-specific parameters and requirements.

