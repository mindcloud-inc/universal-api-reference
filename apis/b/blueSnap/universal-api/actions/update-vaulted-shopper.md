# BlueSnap: Update Vaulted Shopper

Updates a vaulted shopper in BlueSnap.

```
PUT https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-vaulted-shopper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-vaulted-shopper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vaultedShopperId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/update-vaulted-shopper', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vaultedShopperId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vaultedShopperId` | string | yes | ID of the vaulted shopper to update. |
| `firstName` | string | no | Updated shopper first name. |
| `lastName` | string | no | Updated shopper last name. |
| `email` | string | no | Updated shopper email. |
| `country` | string | no | Updated shopper country code (ISO-2). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
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
| `firstName` | string | First name. |
| `lastName` | string | Last name. |
| `shopperCurrency` | string | Shopper currency. |
| `timeCreated` | string | Creation time. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `PUT /vaulted-shoppers/:vaultedShopperId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vaulted-shopper.md) for the provider-specific parameters and requirements.

