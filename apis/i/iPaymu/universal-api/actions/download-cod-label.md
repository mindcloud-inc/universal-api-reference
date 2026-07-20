# iPaymu: Download COD Label

Download the shipping label for an iPaymu cash-on-delivery transaction.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/download-cod-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/download-cod-label?connectionId=$CONNECTION_ID&transaction_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transaction_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/download-cod-label?${params}`, {
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
| `transaction_id` | string | yes | COD transaction identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `GET /cod/download-label/:transaction_id` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-cod-label.md) for the provider-specific parameters and requirements.

