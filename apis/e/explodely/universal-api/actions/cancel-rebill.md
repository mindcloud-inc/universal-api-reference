# Explodely: Cancel Rebill

Cancels rebills in Explodely by main order ID.

```
DELETE https://connect.mindcloud.co/v1/universal/explodely/latest/actions/cancel-rebill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explodely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/explodely/latest/actions/cancel-rebill?connectionId=$CONNECTION_ID&mainOrderId=236084113" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mainOrderId": "236084113"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/explodely/latest/actions/cancel-rebill?${params}`, {
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
| `mainOrderId` | string | yes | The initial Explodely order ID for the rebill sale. Example: `236084113`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "mainorderid": "string",
      "rebillcancel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `mainorderid` | string |  |
| `rebillcancel` | string |  |

## Native endpoint

Through the native Explodely API, this operation is `GET /rebill` (base URL `https://explodely.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-rebill.md) for the provider-specific parameters and requirements.

