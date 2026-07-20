# Column: Get Wire Transfer



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/get-wire-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/get-wire-transfer?connectionId=$CONNECTION_ID&wireTransferId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "wireTransferId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/get-wire-transfer?${params}`, {
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
| `wireTransferId` | string | yes | ID of the wire transfer to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expand` | string | no | Repeatable expansion key for additional wire fields such as raw_message. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `GET /transfers/wire/:wire_transfer_id` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wire-transfer.md) for the provider-specific parameters and requirements.

