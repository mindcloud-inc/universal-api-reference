# Smartcar: Remove Connection

Deletes an existing connection from Smartcar.

```
DELETE https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/remove-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/remove-connection?connectionId=$CONNECTION_ID&connectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/remove-connection?${params}`, {
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
| `connectionId` | string | yes | The unique identifier for the connection to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smartcar API returns.

## Native endpoint

Through the native Smartcar API, this operation is `DELETE /connections/:connectionId` (base URL `https://vehicle.api.smartcar.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-connection.md) for the provider-specific parameters and requirements.

