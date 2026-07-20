# Passslot: Update Pass Price



```
PUT https://connect.mindcloud.co/v1/universal/passslot/latest/actions/update-pass-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Passslot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passslot/latest/actions/update-pass-price" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "passTypeIdentifier": "string",
  "serialNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passslot/latest/actions/update-pass-price', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "passTypeIdentifier": "string",
    "serialNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `passTypeIdentifier` | string | yes | Passslot pass type identifier. |
| `serialNumber` | string | yes | Pass serial number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "price": 1,
      "serialNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `price` | number | Updated pass price. |
| `serialNumber` | string | Pass serial number. |

## Native endpoint

Through the native Passslot API, this operation is `PUT passes/:passTypeIdentifier/:serialNumber/price` (base URL `https://api.passslot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-pass-price.md) for the provider-specific parameters and requirements.

