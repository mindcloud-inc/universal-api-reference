# mintBlue: Create Transaction

Creates a new transaction in mintBlue.

```
POST https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.project_id": "string",
  "params.outputs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.project_id": "string",
    "params.outputs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.project_id` | string | yes | Project ID. |
| `params.outputs[]` | array<object> | yes | Transaction outputs array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.metadata` | object | no | Optional metadata object. |
| `params.rawtx` | boolean | no | Whether to include raw transaction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rawtx": "string",
      "txid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rawtx` | string |  |
| `txid` | string |  |

## Native endpoint

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

