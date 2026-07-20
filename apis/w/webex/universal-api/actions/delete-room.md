# Webex: Delete Room

Deletes an existing room from Webex.

```
DELETE https://connect.mindcloud.co/v1/universal/webex/latest/actions/delete-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webex/latest/actions/delete-room?connectionId=$CONNECTION_ID&roomId=Y2lzY29zcGFyazovL3VzL1JPT00v..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "Y2lzY29zcGFyazovL3VzL1JPT00v..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/delete-room?${params}`, {
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
| `roomId` | string | yes | Room identifier. Example: `Y2lzY29zcGFyazovL3VzL1JPT00v...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Webex API returns.

## Native endpoint

Through the native Webex API, this operation is `DELETE /rooms/:roomId` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-room.md) for the provider-specific parameters and requirements.

