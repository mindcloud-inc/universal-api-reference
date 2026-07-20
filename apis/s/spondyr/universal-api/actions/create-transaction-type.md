# Spondyr: Create Transaction Type

Creates a new transaction type in Spondyr.

```
POST https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/create-transaction-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spondyr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/create-transaction-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "templateJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spondyr/latest/actions/create-transaction-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "templateJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The new transaction type name. |
| `templateJson` | string | yes | Sample JSON payload that defines the transaction type schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "APIStatus": "string",
      "ErrorMessage": "string",
      "ReferenceID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `APIStatus` | string |  |
| `ErrorMessage` | string |  |
| `ReferenceID` | string | Created transaction type identifier. |

## Native endpoint

Through the native Spondyr API, this operation is `POST /TransactionType` (base URL `https://client.spondyr.io/api/v1.0.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction-type.md) for the provider-specific parameters and requirements.

