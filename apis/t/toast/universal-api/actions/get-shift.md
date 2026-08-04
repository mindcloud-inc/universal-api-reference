# Toast: Get Shift

Retrieves one labor shift by Toast GUID or external identifier.

```
GET https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-shift?connectionId=$CONNECTION_ID&shiftId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shiftId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toast/latest/actions/get-shift?${params}`, {
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
| `shiftId` | string | yes | The Toast GUID or external identifier of the shift. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Toast API returns.

## Native endpoint

Through the native Toast API, this operation is `GET /labor/v1/shifts/:shiftId` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shift.md) for the provider-specific parameters and requirements.

