# BlueSnap: Create Vaulted Shopper

Creates a vaulted shopper in BlueSnap.

```
POST https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-vaulted-shopper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-vaulted-shopper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-vaulted-shopper', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "shopperCurrency": "string",
      "timeCreated": "string",
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string | Creation date. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `lastName` | string | Last name. |
| `shopperCurrency` | string | Shopper currency. |
| `timeCreated` | string | Creation time. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `POST /vaulted-shoppers` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vaulted-shopper.md) for the provider-specific parameters and requirements.

