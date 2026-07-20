# Dwolla: Cancel Transfer

Cancels a pending transfer in Dwolla.

```
PUT https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/cancel-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/cancel-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/cancel-transfer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no | Dwolla transfer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "amount": {},
      "created": "string",
      "id": "string",
      "individualAchId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related transfer resources. |
| `amount` | object | Transfer amount and currency. |
| `created` | string | Transfer creation timestamp. |
| `id` | string | Dwolla transfer identifier. |
| `individualAchId` | string | ACH identifier for the transfer when available. |
| `status` | string | Current Dwolla transfer status. |

## Native endpoint

Through the native Dwolla API, this operation is `POST /transfers/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-transfer.md) for the provider-specific parameters and requirements.

