# Skribble: Delete Send-To

Deletes a Send-To request from Skribble.

```
DELETE https://connect.mindcloud.co/v1/universal/skribble/latest/actions/delete-send-to
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/delete-send-to?connectionId=$CONNECTION_ID&accessCode=string&sendToId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessCode": "string",
  "sendToId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/delete-send-to?${params}`, {
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
| `accessCode` | string | yes | The Send-To access code. This will be sent as the X-Accesscode header. |
| `sendToId` | string | yes | The Send-To object ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `DELETE /v2/sendto/:sendToId` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-send-to.md) for the provider-specific parameters and requirements.

